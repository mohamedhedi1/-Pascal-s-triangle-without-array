# -Pascal-s-triangle-without-array
Pascal's triangle in both iterative and recursive methods without array.




















iterative method:
#include<stdio.h>
#include<stdlib.h>
#include<math.h>
int fact (int f);
int num(int n,int p);
void afficher();
int main(){
afficher();
}
int fact(int f)
{
int fa=1,i;
for(i=1;i<=f;i++)
fa=fa*i;
return fa;
}
int num(int n,int p){
return (float)fact(n)/((float)fact(p)*fact(n-p));
}
void afficher()
{
int i,j;
for(i=0;i<19;i++)
{
for(j=0;j<=i;j++)
printf("%4d",num(i,j));
printf("\n");
}
}
recursive method:
#include<stdio.h>
#include<stdlib.h>
#include<math.h>
int fact (int f);
int num(int n,int p);
void afficher();
int main(){
afficher(0,0);
}
int fact(int f)
{
int fa;
if(f<=1)
{fa=1;}
else
{fa=f*fact(f-1);}
return fa;
}
int num(int n,int p){
return (float)fact(n)/((float)fact(p)*fact(n-p));
}
void afficher(int i,int j)
{
if(i<=19)
{
if(j<=i)
    {
      printf("%4d",num(i,j));
      afficher(i,j+1);
    }else
    {
        printf("\n");
        afficher(i+1,0);
    }
}
}

