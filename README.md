## ⭐ Singly Linked List in C++ (5 Marks)

### ✅ Definition:
A singly linked list is a linear data structure where each element (node) contains:
- `data`: stores the value
- `next`: points to the next node

The last node points to `NULL`.

---

### 🔧 Node Structure:
```
struct Node {
    int data;
    Node* next;
};
```

###Insert at Beginning + Print:
```
void insertAtHead(Node*& head, int val) {
    Node* newNode = new Node();
    newNode->data = val;
    newNode->next = head;
    head = newNode;
}

void printList(Node* head) {
    while (head != NULL) {
        cout << head->data << " -> ";
        head = head->next;
    }
    cout << "NULL\n";
}
```

###Main Function:
```
int main() {
    Node* head = NULL;
    insertAtHead(head, 30);
    insertAtHead(head, 20);
    insertAtHead(head, 10);
    printList(head);
    return 0;
}
```

###Output:
```
10 -> 20 -> 30 -> NULL
```

###Summary:

Each node links to the next.

Efficient for dynamic insertion.

Used in memory-efficient applications.
