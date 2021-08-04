#include<stdio.h>
void Reverse(int *arr, int len)      //逆置功能函数，
{
 int tmp;    //存放值
 for (int i = 0; i < len / 2; i++)
 {
  tmp = arr[i];//开始交换

 arr[i] = arr[len - i- 1];
  arr[len - i - 1] = tmp;
 }
}
void Show(int *arr, int len)//打印数组
{
 for (int i = 0; i < len; i++)
 {
  printf("%d\n ", arr[i]);
 }
}
int main()
{
 int arr[5] = { 1,2,3,4,5 };
 int len = sizeof(arr) / sizeof(arr[0]);
 Show(arr,len);
 Reverse(arr,len);
 Show(arr,len);
 return 0;
}
