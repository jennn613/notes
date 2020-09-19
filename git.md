## How to use git



1. git 계정 생성 

2. new repository 생성

3. git과 연동할 폴더 생성

4. READ.me 파일 생성 및 내용 작성

5. 계정 연결

   git init

   git remote add origin (repository address)

   자료 올리는 사람의 이름, 메일 주소 입력

   계정 ID/PW

6. git hub에 push

7. git hub 자료 pull 처리



---



### git 사용법

1. git clone  동기화 폴더 생성

   git clone (git hub 주소)

2. 폴더로 이동

   cd (폴더 이름)

3. 공유 할 파일 생성

4. cat (파일명) > 파일 내용 읽기

5. git 계정 연동

   git config --global user.name "name"

   git config --global user.email "email"

6. 파일 추가

   git add (파일명)

   중간중간 git status로 상태 확인.

7. git commit -m "message"

8. git push

9. git 사이트 확인하기



please enter the message ~ 뜰 때

1. press "i" (i for insert)
2. write your merge message
3. press "esc" (escape)
4. write ":wq" (write & quit)
5. then press enter



제어판 > 사용자 계정 > 자격증명관리 > window 자격증명 git 로그인 관리

git 강제 종료 시 rm -rf .git/index.lock로 잠김 파일 풀어주면 해결

