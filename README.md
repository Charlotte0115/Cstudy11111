#include <stdio.h>
#include <stdlib.h>

void bubble_sort1(int num,int *arr);
void bubble_sort2(int number_len, int* array);

int main(void)
{
    int n = 7;
    int arr[7] = { 0, 25, 10, 17, 6, 12, 9 };
    bubble_sort1(n,arr);
    bubble_sort2(n,arr);
    return 0;
}

void bubble_sort1(int num,int *arr)
{
    int temp;
    int *ptr = malloc(sizeof(int) * num);
    ptr = arr;
    for(int i = 0; i < num; i++) 
    {
        for(int j = 0; j < num-i-1; j++) 
        {
            if(*(ptr + j) > *(ptr + (j + 1)))
            {
                temp = *(ptr + j);
                *(ptr + j) = *(ptr + (j + 1));
                *(ptr + (j + 1)) = temp;
            }
        }
    }
    for(int i = 0; i < num; i++)
    {
        printf("%d",*(ptr+i));
        if(!(i == num - 1)) printf(", ");
    }
    printf("\n");
}
