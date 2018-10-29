# CMcd
magic square
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int i,j;
    int p1[3][3]={{4,9,2},{3,5,7},{8,1,6}};
    int p2[3][3]={{8,3,4},{1,5,9},{6,7,2}};
    int p3[3][3]={{6,1,8},{7,5,3},{2,9,4}};
    int p4[3][3]={{2,7,6},{9,5,1},{4,3,8}};
    int s1=0,s2=0,s3=0,s4=0,s5=0,s6=0,s7=0,s8=0;
    int a[3][3];
    for(i=0;i<3;i++)
        {
        for(j=0;j<3;j++)
            {
            cin>>a[i][j];
            s1+=abs(a[i][j]-p1[i][j]);
            s2+=abs(a[i][j]-p1[i][2-j]);
            s3+=abs(a[i][j]-p2[i][j]);
            s4+=abs(a[i][j]-p2[i][2-j]);
            s5+=abs(a[i][j]-p3[i][j]);
            s6+=abs(a[i][j]-p3[i][2-j]);
            s7+=abs(a[i][j]-p4[i][j]);
            s8+=abs(a[i][j]-p4[i][2-j]);
        }
    }
        int ans=min(min(min(s1,s2),min(s3,s4)),min(min(s5,s6),min(s7,s8)));
        cout<<ans;
    return 0;
}
