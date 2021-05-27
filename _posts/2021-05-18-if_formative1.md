---
layout: single
title: "조건문"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
---
### 서론
C 언어 수업 시간에 교과서를 기반으로 코드를 짠 형성평가 내용

### 01. 사주 보기
문제:
![saju](/assets/images/saju.jpg)   
선생님 코드:
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

내 코드:
~~~c
#include <stdio.h>

int main(void) {
  int year, month, day, last;
  printf("당신의 사주를 봐드립니다.\n연도 월 일을 차례대로 입력하세요 : ");
  scanf("%d %d %d", &year, &month, &day);
  last=(year+month+day)%10;
  if (last==0)
    printf("당신의 사주는 대박입니다.");
  else
    printf("당신의 사주는 그럭저럭입니다.");
  return 0;
}
~~~   

### 02. 3개의 터널 통과
