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
