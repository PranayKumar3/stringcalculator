#include "stdio.h"
#include "stdlib.h"
#include "calc.h"

int compute(char *str)
{
    int k=atoi(str);
    char ch=str[1];
    int m=atoi(str+2);
    if (ch=='+'){
        return k+m;
    }
    else if (ch=='-'){
        return k-m; 
    }
    else if(ch=='*'){
        return k*m;
    }
    else if(ch =='/' && m!=0){
        float ans=(float)k/(float)m;
        return round(ans);
    }
    else
        return 0;
}
