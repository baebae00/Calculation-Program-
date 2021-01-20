# Calculation-Program-
### A calculation program that performs addition, subtraction, and multiplication. 

```python
import time
start=time.time() #프로그램 시작시간

import random #1~99까지의 숫자 랜덤추출을 위한 random함수 선언

count=int(input("암산 능력 강화 프로그램 입니다.\n횟수를 입력하세요: "))
print()

count_right=0 #맞은 개수 0부터 시작
for i in range(1,count+1,1): 
    x=random.randint(1,99) #1~99중 랜덤 추출된 수를 x에 할당
    y=random.randint(1,99) #1~99중 랜덤 추출된 수를 y에 할당
    cal=random.choice(["+","-","*"]) # 뎃셈, 뺄셈, 곱셈 중 랜덤으로 추출된 연산자를cal에 할당
    if cal=="-": #뺄셈 연산자가 추출되면
        print("%s - %s = ?"%(x,y)) #x-y 형식으로 출력됨
        answer=int(input("정답: ")) #사용자가 답을 작성
        if answer==(x-y):
            print("정답입니다.")
            count_right+=1 #정답인 경우 맞은 개수 증가
        else:
            print("오답입니다. 정답은",x-y,"입니다.") #오답인 경우 정답을 알려줌
    elif cal=="+": #덧셈 연산자가 추출되면
        print("%s + %s = ?"%(x,y)) #x+y 형식으로 출력됨
        answer=int(input("정답: "))
        if answer==(x+y):
            print("정답입니다.")
            count_right+=1
        else:
            print("오답입니다. 정답은",x+y,"입니다.")
    else:
        print("%s * %s = ?"%(x,y)) #x*y 형식으로 출력됨
        answer=int(input("정답: "))
        if answer==(x*y):
            print("정답입니다.")
            count_right+=1
        else:
            print("오답입니다. 정답은",x*y,"입니다.")
    print()
        
print("총 ",count,"문제 중",count_right,"개를 맞추셨습니다.") #전체 문제 개수 중 정답의 개수를 출력


finish=time.time() #프로그램이 종료된 시각

t=int(finish-start) #프로그램 종료 시각-프로그램 시작 시각-> 프로그램을 사용하는 데 걸린 시간 

print("총 ",t,"초를 사용하셨습니다.\n수고하셨습니다.") #프로그램을 사용하는 데 걸린 시간을 출력

```
