# c-program-

#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    /* Enter your code here. Read input from STDIN. Print output to STDOUT */ 
    char s[1000];
    gets(s);
    int x[10]={0};
    int i;
    for(i=0;s[i]!='\0';i++)
    {
        if(s[i]>='0'&&s[i]<='9')
        {
            int val=s[i]-'0';
            x[val]=x[val]+1;
            
        }
    }  
    for(i=0;i<10;i++)
    printf("%d ",x[i]); 
    return 0;
}
2nd program
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
//Complete the following function.

int find_nth_term(int n, int a, int b, int c)
{
     if(n==1)
    {
        return a;
    }
    else if(n==2)
    {
        return b;
    }
    else if(n==3)
    {
        return c;
    }
    else
    {
     return find_nth_term(n-1, a, b, c)+find_nth_term(n-2,a,b,c)+find_nth_term(n-3,a,b,c);
    }
}

int main() {
    int n, a, b, c;
  
    scanf("%d %d %d %d", &n, &a, &b, &c); 
    int ans=find_nth_term(n,a,b,c);    
     printf("%d", ans); 
    return 0;
}
