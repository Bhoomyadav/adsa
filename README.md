# adsa
class Node:
    def __init__(self, data):
        self.data, self.next = data, None


head = Node(1)
head.next = Node(2)
head.next.next = Node(3)
head.next.next.next = Node(4)


curr = head
for _ in range(2):   
    curr = curr.next
new = Node(5)
new.next = curr.next
curr.next = new


p = head
while p:
    print(p.data, end=" → ")
    p = p.next
print("null")
