1. 도커 접속

2. ubuntu pull

3. git bash : docker run -it --name ubuntu-python -v //c/rkdtnfla1/digital_twin/ubuntu:/home/ubuntu/data ubuntu bash

    -> 볼륨 설정 (내 pc의 특정 폴더를 공유: 코드 작성이 더 용이함)

4. 기존 pc에서 우분투 폴더 내에 새로운 프로젝트 생성 및 코드 작성

**간단한 프로그램**
```python
menuList = """
[음식의 카테고리를 선택해주세요.]
1. 한식
2. 중식
Q(q): 프로그램 종료
"""

menu1 = """
한식 카테고리입니다.
원하는 음식을 선택하세요.
1. 된찌
2. 제육
3. 소주
B(b): 메인 화면
"""

menu2 = """
중식 카테고리입니다.
원하는 음식을 선택하세요.
1. 짜장
2. 짬뽕
3. 연태
B(b): 메인 화면
"""

if __name__ == '__main__':
    while True:
        print(menuList)
        cmd = input("입력 >>> ")
        if cmd in ("Q", "q"):
            break
        elif cmd == '1':
            while True:
                print(menu1)
                select = input("입력 >>> ")
                if select == '1':
                    print("\n된찌를 선택하였습니다.")
                elif select == '2':
                    print("\n제육을 선택하였습니다.")
                elif select == '3':
                    print("\n소주를 선택하였습니다.")
                elif select in ('B', 'b'):
                    break
                else:
                    print("\n다시 입력하세요.")
        elif cmd == '2':
            while True:
                print(menu2)
                select = input("입력 >>> ")
                if select == '1':
                    print("\n짜장를 선택하였습니다.")
                elif select == '2':
                    print("\n짬뽕을 선택하였습니다.")
                elif select == '3':
                    print("\n연태를 선택하였습니다.")
                elif select in ('B', 'b'):
                    break
                else:
                    print("\n다시 입력하세요.")
        else:
            print("\n다시 입력하세요.")
```

5. 해당하는 언어(apt install python3)를 설치
- Docker에는 sudo 명령어가 없으니 root 계정으로 실행


6. python3 /home/ubuntu/data/src/main/main.py 실행

