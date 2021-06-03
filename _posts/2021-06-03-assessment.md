---
layout: single
title: "수행평가 정리"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
categories: 학교
---
### 서론
수행평가 문항이 될 수업 중 형성평가 내용 정리
### 01. 사주 보기
문제: (출생연도-월+일)의 끝 자리가 0이면 "당신의 사주는 대박입니다.", 0이 아니면 "당신의 사주는 그럭저럭입니다."를 출력
 ~~~c
#include<studio.h>

int main(void) {
  int year, month, day, last;
  printf("당신의 사주를 봐드립니다. 연, 월, 일을 차례로 입력하세요 :");
  scanf("%d%d%d", &year, &month, &day);
  last=(year+month+day)%10;
  if (last==0)
    printf("당신의 사주는 대박입니다.");
  else
    printf("당신의 사주는 그럭저럭입니다.");
  return 0;
}
~~~   
   
### 02. 3개의 터널 통과
세 터널의 높이를 차례로 입력했을 때 터널이 높아 무사히 지나갈 수 있으면 "무사 통과", 터널이 낮아 충돌하면 "충돌"과 함꼐 가장 처음 충돌한 터널의 높이를 출력

   
### 03. 이 달은 며칠까지 있을까?
연도와 달을 입력받고 윤년을 고려하여 그 달이 며칠까지 있는지 출력
   
    
### 04. 30분 전
시간과 분을 입력받고 입력 받은 시간의 30분 전 시간을 출력
~~~c
#include <stdio.h>

int main(void) {
  int hour, minute, minutep;
  printf("시간과 분을 입력하세요 :");
  scanf("%d%d", &hour, &minute);
  printf("입력한 시간의 30분 전 시각은");
  if (minute>=30)
    printf("%d시 %d분", hour, minute-30);
  else
    {if (hour==0)
    printf("%d시 %d분", 23, 30+minute);
    else
    printf("%d시 %d분", hour-1, 30+minute);}
  return 0;
}
~~~
   
### 05. 책 구입
용돈을 입력받고 그 용돈으로 책을 살 수 있으면 "책을 살 수 있습니다."와 남은 용돈, 살 수 없으면 "책을 살 수 없습니다."를 출력
   
### 06. 도어락
ic, 비밀번호, 지문으로 열 수 있는 도어락이 열리면 "문 열림~", 열리지 않으면 "디리릭!"을 출력
~~~c
#include <stdio.h>

int main(void) {
  char ic;
  int pw;
  double pf;
  int method;
  printf("ic카드(1)나 비밀번호(2)나 지문(3) 중 인증 방법을 선택하세요 :");
  scanf("%d", &method);
  if (method==1){
    printf("ic카드 :");
   scanf(" %c", &ic);
     if (ic=='c')
     {printf("문 열림~");}
     else
     {printf("디리릭!");}}
  if(method==2) {
    printf("비밀번호 :");
    scanf(" %d", &pw);
    if (pw==24689)
      printf("문 열림~");
    else 
    printf("디리릭!"); }
  if(method==3)
    printf("지문 :");
    scanf("%lf", &pf);
    if (pf==1.2345678)
      printf("문 열림~");
    else
      printf("디리릭!");
  return 0;
}
~~~
   
### 07. 등급 나누기
점수를 입력 받으면 해당하는 등급을 출력
   
### 08. 가위바위보
r, s, p 중 하나를 입력받고 "이겼다", "졌다", "비겼다"를 출력 (랜덤으로 r, s, p를 지정해야하지만 그냥 미리 컴퓨터의 r, s, p 값을 지정해두고 코드를 짬)
~~~c
#include <stdio.h>

int main(void) {
  char hand;
  char hand2='s';
  printf("입력(가위:s, 바위:r, 보:p):");
  scanf("%c" , &hand);
  if (hand==hand2)
    printf("비겨따!");
  else
    {if ((hand=='r' && hand2=='s')|| (hand=='s'&&hand2=='p')|| (hand=='p'&&hand=='r'))
       printf("이겨따!");
     else
       printf("져따!");}
  return 0;
}
~~~
