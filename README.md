# mini-project-to-findday-on-given-date.c-
// c mini-project to findday on given date.

// c mini-project to findday on given date.
#include <stdio.h>

int main() {
    int d,m,gy,y1,y2,y3,q1,q2,q3,l,sum=0,s,i,d1;
    printf("enter day ,month and year=");
    scanf("%d%d%d",&d,&m,&gy);
    
    y1=(gy-1)%400;
    q1=((gy-1)/400)*0;

    
    y2=y1%100;
    q2=(y1/100)*5;

    y3=y2%4;
    q3=(y2/4)*1;

    if(gy%400 == 0)
     l=1;
    else if(gy%100 == 0)
     l=0;
    else if(gy%4 == 0)
     l=1;
    else
     l=0;
     
    if(l){
     int mm[]={3,1,3,2,3,2,3,3,2,3,2,3};
      for(i=0;i<m-1;i++)
       sum=sum+mm[i];
    }
    else{
     int mm[]={3,0,3,2,3,2,3,3,2,3,2,3};
     for(i=0;i<m-1;i++)
      sum=sum+mm[i];
    }

    s=q1+q2+q3+y2+sum+d;
    
    d1=s%7;
    
    switch (d1) {
    case 0:
      printf("Sunday\n");
      break;
    case 1:
      printf("Monday\n");
      break;
    case 2:
      printf("Tuesday\n");
      break;
    case 3:
      printf("Wednesday\n");
      break;
    case 4:
      printf("Thursday\n");
      break;
    case 5:
      printf("Friday\n");
      break;
    case 6:
      printf("Saturday\n");
      break;
  }
    return 0;
}

