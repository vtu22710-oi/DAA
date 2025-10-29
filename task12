Task 12a
#include<stdio.h>
#include<conio.h>
int s[10],d,n,set[10],count=0;
void display(int);
int flag = 0;
void main()
{
 int subset(int,int);
 int i;
 clrscr();
 printf("ENTER THE NUMBER OF THE ELEMENTS IN THE SET : ");
 scanf("%d",&n);
 printf("ENTER THE SET OF VALUES : ");
 for(i=0;i<n;i++)
   scanf("%d",&s[i]);
 printf("ENTER THE SUM : ");
 scanf("%d",&d);
 printf("THE PROGRAM OUTPUT IS: ");
 subset(0,0);
 if(flag == 0)
 printf("There is no solution");
 getch();
}
int subset(int sum,int i)
{
if(sum == d)
{
 flag = 1;
 display(count);
 return;
}
if(sum>d || i>=n)return;
else
{
 set[count]=s[i];
 count++;
 subset(sum+s[i],i+1);
 count--;
 subset(sum,i+1);
}}
void display(int count)
{
 int i;
 printf("\t{");
 for(i=0;i<count;i++)
 printf("%d,",set[i]);
 printf("}");
}

Task 12b
#include <stdio.h>
#include <stdlib.h>
static int total_nodes;
void printValues(int A[], int size)
{ 
for (int i = 0; i < size; i++) 
{
 printf("%*d", 5, A[i]);
 } 
printf("\n");}
void subset_sum(int s[], int t[], int s_size, int t_size, int sum, int ite, int const target_sum)
{
 total_nodes++; 
if (target_sum == sum) 
{
 printValues(t, t_size);
 subset_sum(s, t, s_size, t_size - 1, sum - s[ite], ite + 1, target_sum); 
return; 
} 
else 
{
 for (int i = ite; i < s_size; i++) 
{ 
t[t_size] = s[i]; 
subset_sum(s, t, s_size, t_size + 1, sum + s[i], i + 1, target_sum);
 } 
}
}
void generateSubsets(int s[], int size, int target_sum)
{
 int* tuplet_vector = (int*)malloc(size * sizeof(int)); subset_sum(s, tuplet_vector, size, 0, 0, 0, target_sum); free(tuplet_vector);
}
int main()
{
 int set[] = { 5, 6, 12 , 54, 2 , 20 , 15 }; 
int size = sizeof(set) / sizeof(set[0]);
 printf("The set is "); 
printValues(set , size);
 generateSubsets(set, size, 25); 
printf("Total Nodes generated %d\n", total_nodes); return 0;
}

Task 12c
#include <stdio.h>
#include <stdlib.h>

int arr[N]
void allSubsets(int pos, int len, int[] subset) {
  if (pos == N) //position
  {
    print(subset)
    return
  }
  subset[len] = arr[pos]
  //take element
  allSubsets(pos + 1, len + 1, subset)
  // Skip the current element.
  allSubsets(pos + 1, len, subset)
}
