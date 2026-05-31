# EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST

## Aim:

To write a C program to display stack elements using linked list.

## Algorithm:

1. Define a structure Node with two members: data and next.
2. Declare a global variable head.
3. Define a display function.
4. Initialize pointer p with head.
5. Traverse using while loop.
6. Print node data.
7. Move pointer to next node.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *head = NULL;

void push(int value)
{
    struct Node *newnode;

    newnode = (struct Node*)malloc(sizeof(struct Node));

    newnode->data = value;
    newnode->next = head;
    head = newnode;
}

void display()
{
    struct Node *p = head;

    while(p != NULL)
    {
        printf("%d ", p->data);
        p = p->next;
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    display();

    return 0;
}
```

## Output:

```text
30 20 10
```

## Result:

Thus, the program to display stack elements using linked list is verified successfully.

# EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST

## Aim:

To write a C program to pop an element from the given stack using linked list.

## Algorithm:

1. Check for empty stack.
2. If head is NULL print stack empty.
3. Else continue.
4. Move head to next node.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *head = NULL;

void push(int value)
{
    struct Node *newnode;

    newnode = (struct Node*)malloc(sizeof(struct Node));

    newnode->data = value;
    newnode->next = head;
    head = newnode;
}

void pop()
{
    if(head == NULL)
    {
        printf("Stack is empty");
    }
    else
    {
        struct Node *temp = head;

        printf("Popped element = %d", head->data);

        head = head->next;

        free(temp);
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    pop();

    return 0;
}
```

## Output:

```text
Popped element = 30
```

## Result:

Thus, the program to pop an element from the given stack using linked list is verified successfully.

# EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST

## Aim:

To write a C program to display queue elements using linked list.

## Algorithm:

1. Check if queue is empty.
2. Display queue elements.
3. Print current node data.
4. Move front to next node.
5. End display function.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front = NULL, *rear = NULL;

void enqueue(int value)
{
    struct Node *p;

    p = (struct Node*)malloc(sizeof(struct Node));

    p->data = value;
    p->next = NULL;

    if(front == NULL)
    {
        front = rear = p;
    }
    else
    {
        rear->next = p;
        rear = p;
    }
}

void display()
{
    struct Node *temp = front;

    while(temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    return 0;
}
```

## Output:

```text
10 20 30
```

## Result:

Thus, the program to display queue elements using linked list is verified successfully.

# EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

## Aim:

To write a C program to insert elements in queue using linked list.

## Algorithm:

1. Allocate memory for new node.
2. Set data and next pointer.
3. Check whether queue is empty.
4. Assign front and rear to new node.
5. Connect rear next to new node.
6. Finish enqueue operation.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front = NULL, *rear = NULL;

void enqueue(int value)
{
    struct Node *p;

    p = (struct Node*)malloc(sizeof(struct Node));

    p->data = value;
    p->next = NULL;

    if(front == NULL)
    {
        front = rear = p;
    }
    else
    {
        rear->next = p;
        rear = p;
    }
}

void display()
{
    struct Node *temp = front;

    while(temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    enqueue(5);
    enqueue(15);
    enqueue(25);

    display();

    return 0;
}
```

## Output:

```text
5 15 25
```

## Result:

Thus, the program to insert elements in queue using linked list is verified successfully.

# EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST

## Aim:

The aim of this function is to retrieve the peek element of a queue implemented using a linked list.

## Algorithm:

1. Check whether queue is empty.
2. If front is NULL print queue empty.
3. Otherwise print front node data.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front = NULL, *rear = NULL;

void enqueue(int value)
{
    struct Node *p;

    p = (struct Node*)malloc(sizeof(struct Node));

    p->data = value;
    p->next = NULL;

    if(front == NULL)
    {
        front = rear = p;
    }
    else
    {
        rear->next = p;
        rear = p;
    }
}

void peek()
{
    if(front == NULL)
    {
        printf("Queue is empty");
    }
    else
    {
        printf("Peek element = %d", front->data);
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    peek();

    return 0;
}
```

## Output:

```text
Peek element = 10
```

## Result:

Thus, the program to retrieve the peek element of a queue implemented using a linked list is verified successfully.
