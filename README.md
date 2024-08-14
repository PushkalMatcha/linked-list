# linked-list
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

int main() {
    int value;
    struct Node* node = (struct Node*)malloc(sizeof(struct Node));
    
    if (node == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }
    
    printf("Enter a value for the node: ");
    scanf("%d", &value);
    
    node->data = value;
    node->next = NULL;
    
    printf("Node data: %d\n", node->data);
    
    free(node);
    return 0;
}
