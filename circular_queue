#include <stdio.h>
#define SIZE 5

int q[SIZE], front = 0, rear = -1, count = 0;

void insert(int x) {
    if (count == SIZE) { printf("Queue Full\n"); return; }
    rear = (rear + 1) % SIZE;
    q[rear] = x;
    count++;
}

void delete() {
    if (count == 0) { printf("Queue Empty\n"); return; }
    printf("Deleted: %d\n", q[front]);
    front = (front + 1) % SIZE;
    count--;
}

void display() {
    printf("Circular Queue: ");
    for (int i = 0; i < count; i++)
        printf("%d ", q[(front + i) % SIZE]);
    printf("\n");
}

int main() {
    insert(10); insert(20); insert(30); insert(40); 
    delete(); delete();                              
    insert(50); insert(60);                          
    display();                                      
    return 0;
}
