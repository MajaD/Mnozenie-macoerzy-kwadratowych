Mnozenie-macoerzy-kwadratowych
==============================
#include<stdio.h>
int main()
{
    int tab1[25][25];
    int tab2[25][25];
    int tab3[25][25];
    int a,b,c,w,z,x,v,n,pomoc;
    c=1;
    printf("podaj wielkosc macierzy kwadratowej: \n");
    scanf("%d", &w);
    printf("podaj liczby pierwszej macierzy: \n");
    for(a=0;a<w;a++)
    {
        for(b=0;b<w;b++)
        {
            printf("liczba %3d:  ", c);
            scanf("%d", &tab1[a][b]);
            c++;
        }
        
    }
    printf("podaj liczby drugiej macierzy: \n");
    c=1;
    for(a=0;a<w;a++)
    {
        for(b=0;b<w;b++)
        {
            printf("liczba %3d:  ", c);
            scanf("%d", &tab2[a][b]);
            c++;
        }
        
    }
    for(x=0;x<w;x++)
    {
        for(z=0;z<w;z++)
        {
    a=0;
    b=0;
    pomoc=0;
    while (a<w && b<w)
    {
        pomoc=((tab1[x][b]*tab2[a][z]) + pomoc);
        b=b+1;
        a=a+1;
    }
    tab3[x][z]=pomoc;
    }
    }
    n=0;
    v=w/2;
    for(a=0;a<w;a++)
    {
        for(b=0;b<w;b++)
        {
            printf("%3d", tab1[a][b]);
        }
        if(n==v)
        {
        printf(" * ");
        }
        else
        {
            printf("   ");
        }
        for(b=0;b<w;b++)
        {
            printf("%3d", tab2[a][b]);
        }
        if(n==v)
        {
        printf(" = ");
        }
        else
        {
            printf("   ");
        }
        for(b=0;b<w;b++)
        {
            printf("%3d", tab3[a][b]);
        }
        printf("\n");
        n=n+1;
    }
    }
