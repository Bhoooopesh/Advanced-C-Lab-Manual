# EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

## Aim:

To write a C program to create a function to find the greatest number.

## Algorithm:

1. Include the header file stdio.h.
2. Use if and else if statements to compare the values.
3. Declare variables n1, n2, n3, n4, and greater.
4. Use scanf to get four integer inputs.
5. Call the max_of_four function and store the result.
6. Print the greatest number.

## Program:

```c
#include <stdio.h>

int max_of_four(int a, int b, int c, int d)
{
    if(a>b && a>c && a>d)
        return a;
    else if(b>c && b>d)
        return b;
    else if(c>d)
        return c;
    else
        return d;
}

int main()
{
    int n1, n2, n3, n4, greater;

    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);

    greater = max_of_four(n1, n2, n3, n4);

    printf("Greatest number = %d", greater);

    return 0;
}
```

## Output:

```text
12 45 23 18
Greatest number = 45
```

## Result:

Thus, the program that create a function to find the greatest number is verified successfully.

# EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND XOR COMPARISONS

## Aim:

To write a C program to print the maximum values for the AND, OR and XOR comparisons.

## Algorithm:

1. Define a function calculate_the_max with parameters n and k.
2. Declare variables a, o, and x.
3. Use nested loops to compare all pairs.
4. Update maximum AND, OR, and XOR values.
5. Get input values using scanf.
6. Call the function.
7. Print the results.

## Program:

```c
#include <stdio.h>

void calculate_the_max(int n, int k)
{
    int a = 0, o = 0, x = 0;

    for(int i = 1; i <= n; i++)
    {
        for(int j = i + 1; j <= n; j++)
        {
            if((i & j) < k && (i & j) > a)
                a = (i & j);

            if((i | j) < k && (i | j) > o)
                o = (i | j);

            if((i ^ j) < k && (i ^ j) > x)
                x = (i ^ j);
        }
    }

    printf("%d\n", a);
    printf("%d\n", o);
    printf("%d\n", x);
}

int main()
{
    int n, k;

    scanf("%d %d", &n, &k);

    calculate_the_max(n, k);

    return 0;
}
```

## Output:

```text
5 4
2
3
3
```

## Result:

Thus, the program to print the maximum values for the AND, OR and XOR comparisons is verified successfully.

# EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

## Aim:

To write a C program to write the logic for the requests.

## Algorithm:

1. Declare variables noshel and noque.
2. Get the number of shelves and queries.
3. Declare arrays for shelves and books.
4. Use variables k and c for indexing.
5. Use a loop to process queries.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int noshel, noque;

    scanf("%d", &noshel);
    scanf("%d", &noque);

    int *nobookarr = (int *)calloc(noshel, sizeof(int));
    int **shelarr = (int **)malloc(noshel * sizeof(int *));

    while(noque--)
    {
        int type;
        scanf("%d", &type);

        if(type == 1)
        {
            int x, y;
            scanf("%d %d", &x, &y);

            int k = nobookarr[x];

            shelarr[x] = (int *)realloc(shelarr[x], (k + 1) * sizeof(int));

            shelarr[x][k] = y;

            nobookarr[x]++;
        }
        else if(type == 2)
        {
            int x, y;
            scanf("%d %d", &x, &y);

            printf("%d\n", shelarr[x][y]);
        }
        else
        {
            int x;
            scanf("%d", &x);

            printf("%d\n", nobookarr[x]);
        }
    }

    return 0;
}
```

## Output:

```text
5
5
1 0 15
1 0 20
1 1 30
2 0 1
3 0

20
2
```

## Result:

Thus, the program to write the logic for the requests is verified successfully.

# EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY

## Aim:

To write a C program print the sum of the integers in the array.

## Algorithm:

1. Declare variable n.
2. Get input for n.
3. Declare array a.
4. Initialize sum as 0.
5. Use loop to input elements.
6. Add elements to sum.
7. Print the sum.

## Program:

```c
#include <stdio.h>

int main()
{
    int n, sum = 0;

    scanf("%d", &n);

    int a[n];

    for(int i = 0; i < n; i++)
    {
        scanf("%d", &a[i]);
        sum = sum + a[i];
    }

    printf("%d", sum);

    return 0;
}
```

## Output:

```text
5
10 20 30 40 50
150
```

## Result:

Thus, the program prints the sum of the integers in the array is verified successfully.

# EXP NO:25 C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

## Aim:

To write a C program that counts the number of words in a given sentence.

## Algorithm:

1. Input the sentence.
2. Initialize word count variable.
3. Traverse each character in the sentence.
4. Count words separated by spaces.
5. Print the total word count.

## Program:

```c
#include <stdio.h>
#include <string.h>

int main()
{
    char str[100];
    int count = 0;

    fgets(str, sizeof(str), stdin);

    for(int i = 0; str[i] != '\0'; i++)
    {
        if((i == 0 && str[i] != ' ') || (str[i] != ' ' && str[i - 1] == ' '))
        {
            count++;
        }
    }

    printf("Number of words = %d", count);

    return 0;
}
```

## Output:

```text
Welcome to C programming
Number of words = 4
```

## Result:

Thus, the program that counts the number of words in a given sentence is verified successfully.
