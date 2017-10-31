# Even-sum

Even sum

Problem Description

有一个长度为n(n<=100)的数列，该数列定义为从2开始的递增有序偶数，现在要求你按照顺序每m个数求出一个平均值，如果最后不足m个，则以实际数量求平均值。编程输出该平均值序列。 


Input

输入数据有多组，每组占一行，包含两个正整数n和m，n和m的含义如上所述。

 
Output

对于每组输入数据，输出一个平均值序列，每组输出占一行。

 
Sample Input

3 2

4 2 


Sample Output

3 6

3 7


解答：

#include<stdio.h>

main()

{

    int n,m,a,b,i,j,k,w,l,e,s,d,r;
    
    while(scanf("%d%d",&n,&m)!=EOF)
    
    {
    
         s=0;
         
         e=0;
         
         l=0;
         
         if(n<=m)
         
         {
         
            for(i=0;i<n;i++)
            
            {
            
            s=s+2;
            
            e=e+s;
            
            k=e/n;
            
            }
            
            printf("%d\n",k);
            
         }
         
         else
         
         {
         
            w=n%m;
            
            r=0;
            
            for(i=1;i<=n-w;i++)
            
            {
                       
            s=s+2;
            
            l=l+s;
            
            e=e+s;
            
            if(i%m==0)
            
             {
             
             k=e/m;
             
             e=0;
             
             if(r)
             
              printf(" ");
              
             printf("%d",k);
             
              r=r+1;
              
             }
             

            }
            
            s=0;
            
            if(w!=0)
            
            {
            
            for(j=0;j<n;j++)
            
            {
            
                s=s+2;
                
                e=e+s;
                

            }
            

            d=e-l;
            
            k=d/w;
            
             printf(" ");
             
            printf("%d",k);
            
            }
            
            printf("\n");
            
         }
         

    }
    
}

