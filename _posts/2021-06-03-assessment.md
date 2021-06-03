---
layout: single
title: "수행평가 정리"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
categories: “형성평가”
---

### 01. 사주보기

~~~c
#include <stdio.h>
int main(void)
{ int year,month,day,result;
printf("당신의 사주를 봐드립니다.\n");
printf("연도 월 일을 차례대로 입력하세요 : ");
scanf("%d,%d,%d",&year,&month,&day);
result=(year-month+day)%10;
if(result==0)
printf("당신의 사주는 대박입니다.\n");
else
printf("당신의 사주는 그럭저럭입니다.\n");
return 0;
}
~~~

### 02. 터널통과

~~~c
#include <stdio.h>
int main(void)
{ int tunnul_1, tunnul_2, tunnul_3;
printf("세 터널의 높이를 차례대로 입력하세요 : ");
scanf("%d,%d,%d",&tunnul_1,&tunnul_2,&tunnul_3);
if(tunnul_1<=170)
printf("충돌 %d", tunnul_1);
else if(tunnul_2<=170)
printf("충돌 %d", tunnul_2);
else if(tunnul_3<=170)
printf("충돌 %d", tunnul_3);
else
printf("무사 통과");
return 0;
}
~~~

### 03. 이달은 며칠까지 있을까?
~~~c
#include <stdio.h>
int main() {
  int a,b;
  printf("연도와 월을 입력하세요\n");
  scanf("%d %d", &a, &b);
  printf("%d년 %d월의 마지막 날은 ", a, b);
   if  (b==2 && a %4 == 0 && a% 100!=0)
  printf("윤년이므로 29일입니다.");
  else if (b==2)
  printf("28일입니다.");
  if (!(b==2 || b==4 || b==6 || b==9 || b==11))
    printf("31일");
   else if (!(b==2))
    printf("30일");
  return 0;
}
~~~

### 04. 30분 전
~~~c
#include <stdio.h>
int main() {
  int 시간, 분;
  printf("시간과 분을 입력하세요 :\n");
  scanf("%d %d", &시간, &분);
 printf("입력한 시간의 30분 전 시간은");
 if (분 >= 30){
   printf("%d시 %d분\n", 시간, 분-30);
 }
 if (시간 == 0){
   printf("%d시 %d분\n", 23, 분+30);
 } else{
 printf("%d시 %d분", 시간-1, 분+30);
 } 
  return 0;
}
~~~

### 05. 도어락
~~~c
#include <stdio.h>

int main() 
{  double a;
  char b;
  int c, d;
  printf(">>>테스트\n IC카드는 1, 비밀번호는 2 지문입력은 1,2를 제외한 수를 입력하시오\n");
  scanf("%d", &d);
if (d==1)
{
  printf("IC카드 값: ");
    scanf("%s", &b);
}
 else if (d==2)
{
  printf("비밀번호: ");
    scanf("%d", &c);
}
 else 
 {
   printf("지문 입력: ");
    scanf("%lf", &a);
}
    if (!(a == 1.2345678 || b=='c' || c==24680))
     {
   printf("디리릭! 디리릭!\n");
    } 
    else
    {
  printf("문열림\n");
    }
  return 0;
}
~~~


### 06. 가위바위보
~~~c
#include <stdio.h>
int main() {
  char a,b;
  printf("가위 바위 보 중 하나를 선택하시오\n");
  scanf("%s", &a);
  if (a==b) {
   printf("비겼다");  
  } else if ((b=='r' && a=='s') || (b=='s'&& a=='p') ||(b=='p'&& a=='r')) {
   printf("졌다.");
  } else  {
    printf("이겼다.");
  }
  return 0;
}
~~~
