#include <assert.h>
#include <limits.h>
#include <math.h>
#include <stdbool.h>
#include <stddef.h>
#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
void lrot(int n,int d,int a[])
{
    int res[n];
    if(d==n || d==0)
    {
        for(int i=0;i<n;i++)
        {
            printf("%d ",a[i]);
        }
    }
    else{
        for(int j=0;j<d;j++)
        {
            res[n-1]=a[0];
            for(int i=0;i<n-1;i++)
            {
                res[i]=a[i+1];
            }
            for(int i=0;i<n;i++)
            {
                a[i]=res[i];
            }
        }
        for(int i=0;i<n;i++)
            {
                printf("%d ",res[i]);
            }
    }
}
int main()
{
    int n,d;
    scanf("%d %d",&n,&d);
    int a[n];
    if(1<=d && d<=n)
    {
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    lrot(n,d,a);
    }
    return 0;
}
