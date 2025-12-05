# Linked-list
Linked list and dictionary 
# Node class
class Node:
    def __init__(self, data):
        self.data = data      # data is a dictionary
        self.next = None      # pointer to next node

# Linked List class
class LinkedList:
    def __init__(self):
        self.head = None

    # insert at end
    def insert(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            return

        current = self.head
        while current.next:
            current = current.next
        current.next = new_node

    # display linked list
    def display(self):
        current = self.head
        while current:
            print(current.data)
            current = current.next


# -----------------------------
# USING THE LINKED LIST
# -----------------------------

students = LinkedList()

# Adding one student as example
student1 = {
    "name": "Salma Chesang",
    "admission": "CIT/0234",
    "grades": {
        "unit1": 78,
        "unit2": 85,
        "unit3": 90
    }
}

students.insert(student1)

# Add more students to test the linked list
student2 = {
    "name": "Mwero Faith",
    "admission": "CIS/0081/024",
    "grades": {
        "unit1": 67,
        "unit2": 85,
        "unit3": 70,
    }
}
students.insert(student2)

student3 = {
    "name": "Ondiege Linet",
    "admission": "CIT/0046/024",
    "grades": {
        "unit1":80,
        "unit2": 45,
        "unit3": 87,
    }
}
students.insert(student3)

students.display()
