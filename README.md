# Day56.
My c language daily practice 
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int *ptr;
    int n = 5;

    ptr = (int*)malloc(n * sizeof(int));

    if (ptr == NULL)
    {
        printf("Memory not allocated");
        return 1;
    }

    printf("Enter 5 numbers:\n");

    for(int i = 0; i < n; i++)
    {
        scanf("%d", &ptr[i]);
    }

    printf("Numbers are:\n");

    for(int i = 0; i < n; i++)
    {
        printf("%d ", ptr[i]);
    }

    free(ptr);

    return 0;
}
