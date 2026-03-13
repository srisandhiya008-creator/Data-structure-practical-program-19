class Node:
    def __init__(self,id,name,marks):
        self.id=id
        self.name=name
        self.marks=marks
        self.next=None

class LinkedList:
    def __init__(self):
        self.head=None

    def insert(self,id,name,marks):
        new=Node(id,name,marks)
        new.next=self.head
        self.head=new

    def search(self,id):
        t=self.head
        while t:
            if t.id==id:
                print(t.id,t.name,t.marks)
            t=t.next

    def display(self):
        t=self.head
        while t:
            print(t.id,t.name,t.marks)
            t=t.next

L=LinkedList()
L.insert(1,"Ram",85)
L.insert(2,"Sam",90)

L.display()
print("Search:")
L.search(1)# Data-structure-practical-program-19
