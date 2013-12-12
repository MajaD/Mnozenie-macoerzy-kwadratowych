Mnozenie-macierzy-kwadratowych
==============================
1.#include<stdio.h>
2.int main()

3. {
4.    int tab1[25][25];
5.    int tab2[25][25];
6.    int tab3[25][25];
7.    int a,b,c,w,z,x,v,n,pomoc;
8.    c=1;
9.    printf("podaj wielkosc macierzy kwadratowej: \n");
10.    scanf("%d", &w);
11.    printf("podaj liczby pierwszej macierzy: \n");
12.    for(a=0;a<w;a++)
13.    {
14.        for(b=0;b<w;b++)
15.        {
16.            printf("liczba %3d:  ", c);
17.            scanf("%d", &tab1[a][b]);
18.            c++;
19.        }
20.     }
21.    printf("podaj liczby drugiej macierzy: \n");
22.   c=1;
23.    for(a=0;a<w;a++)
24.    {
25.       for(b=0;b<w;b++)
26.        {
27.            printf("liczba %3d:  ", c);
28.            scanf("%d", &tab2[a][b]);
29.            c++;
30.        }
31.        
32.    }
33.    for(x=0;x<w;x++)
34.    {
35.        for(z=0;z<w;z++)
36.        {
37.    a=0;
38.    b=0;
39.    pomoc=0;
40.    while (a<w && b<w)
41.    {
42.        pomoc=((tab1[x][b]*tab2[a][z]) + pomoc);
43.        b=b+1;
44.        a=a+1;
45.    }
46.    tab3[x][z]=pomoc;
47.    }
48.    }
49.    n=0;
50.    v=w/2;
51.    for(a=0;a<w;a++)
52.    {
53.        for(b=0;b<w;b++)
54.        {
55.            printf("%3d", tab1[a][b]);
56.        }
57.        if(n==v)
58.        {
59.        printf(" * ");
60.        }
61.        else
62.        {
63.            printf("   ");
64.        }
65.        for(b=0;b<w;b++)
66.        {
67.            printf("%3d", tab2[a][b]);
68.        }
69.        if(n==v)
70.        {
71.            printf(" = ");
72.        }
73.        else
74.        {
75.            printf("   ");
76.        }
77.        for(b=0;b<w;b++)
78.        {
79.            printf("%3d", tab3[a][b]);
80.        }
81.        printf("\n");
82.        n=n+1;
83.    }
84.    }

