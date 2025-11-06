#include <stdio.h>
#include <stdlib.h>
struct Node {
    int data;
    struct Node* next;
};
struct Node* head = NULL;
// Function to insert node at a specific position
void insertPos(int value, int pos) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    if (!newNode) {
        printf("Memory allocation failed\n");
        return;
    }
    newNode->data = value;
    if (pos == 1) { // Insert at beginning
        newNode->next = head;
        head = newNode;
        return;
    }
    struct Node* temp = head;
    for (int i = 1; i < pos - 1 && temp != NULL; i++)
        temp = temp->next;
    if (temp == NULL) {
        printf("Position out of range!\n");
        free(newNode);
        return;
    }
    newNode->next = temp->next;
    temp->next = newNode;
}
// Function to display linked list
void display() {
    struct Node* temp = head;
    if (temp == NULL) {
        printf("List is empty.\n");
        return;
    }
    while (temp != NULL) {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    printf("NULL\n");
}
int main() {
    insertPos(10, 1);  // Insert at position 1
    insertPos(20, 2);  // Insert at position 2
    insertPos(30, 3);  // Insert at position 3
    insertPos(15, 2);  // Insert at position 2
    insertPos(5, 1);   // Insert at position 1
    printf("Linked List after insertions:\n");
    display();
    return 0;
}
