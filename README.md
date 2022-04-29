# 터미널 깃허브 연동방법
## _1. 깃허브에서 레파지토리를 생성한다._
1.1. github.com 접속

1.2. new 클릭

1.3. 레퍼지터리 이름 작성

1.4. Public / Private 선택

1.5. Create Repository 클릭

## _2. 깃 레파지토리 주소를 복사해둔다._
2.1. Code 클릭

2.2. HTTPS 선택

2.3. 복사 버튼 클릭

## _3. 터미널을 켜고, 프로젝트 폴더로 진입한다._
3.1. 윈도우, 맥, 리눅스에서 사용 중인 터미널을 연다.

3.2. Android Studio, Visual Studio Code 등에서 제공되는 터미널을 열어도 된다.

3.3. 안드로이드 스튜디오, 비쥬얼 스튜디오 코드 등의 IDE에서 터미널을 연다면, 보통 프로젝트 경로에서 열린다.

## _4. 깃 명령어 입력_
4.1. git 초기화:  git init 

4.2. 모든 폴더/파일을 Staging 추가:  git add . 

4.3. 커밋:  git commit -m '커밋 메시지' 

4.4. 레퍼지터리(원격저장소) 연결:  git remote add origin 원격저장소URL 
- 4.4.1. 원격저장소 URL 항목에 아까 github에서 복사해둔 https://github.com/계정/레퍼지터리.git 을 입력하면 된다.
- 4.4.2. 기본 명령어 형식은 git remote add 원격저장소별칭 원격저장소URL이며, 별칭은 보통 origin을 많이 쓴다.
- 4.4.3. git remote -v 명령어를 입력하면, 원격저장소에 잘 연결되어있는지 확인이 가능하다.

4.5.Git Hub에 최초 푸시(업로드):  git push -u origin master
- 4.5.1. 명령어 형식은 git push -u 원격저장소별칭 브랜치명 이며, 브랜치명은 주로 master나 main을 많이 쓴다.

위 작업 과정 중에 비밀번호 혹은 PAT(Personal Access Token)를 입력라는 메시지가 나올 수 있다.
ID와 PW는 각각 Git Hub의 아이디와 비밀번호를 입력하면 된다.
만약 Personal Access Token을 사용하는 메시지가 나오면, 아래 글을 참고하여 PAT를 만들어서 사용하면 된다.(쉬움)
GitHub 토큰 인증 로그인: Personal Access Token [생성 및 사용 방법][gitToken]

## _5. 이후 작업_
위까지 작업을 해두면, 향후 작업은 add, commit, push, pull 의 반복이다.

5.1. staging 추가:  git add .

5.2. 커밋: git commit -m '커밋메시지'

5.3. 푸시(업로드): git push

최초에 -u를 붙여 푸시한 다음에는, 간단하게 git push만 입력해도 된다.

5.4. 풀(다운로드): git pull

5.5. .gitignore 파일 생성: git 추적 제외 파일/폴더 설정
용량이 큰 라이브러리나 민감한 주요 설정 정보 파일 등의 경우, git의 추적에서 제외할 필요가 있을 수 있다.
git의 추적에서 제외할 폴더나 파일이 있는 경우,
프로젝트 폴더에 .gitignore 이름의 파일을 생성해두고, 아래와 같이 작성해두면 된다.

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
   [gitToken]: <https://curryyou.tistory.com/344>
