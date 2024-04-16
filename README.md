# My-blog-app

## 프로젝트 소개
express 학습을 위한 개인 프로젝트 입니다. 간단한 강의를 참고하여 블로그를 제작해보았습니다.
<img width="1350" alt="스크린샷 2024-04-16 오후 1 43 09" src="https://github.com/Jeong-wonho/my-blog-app/assets/67899479/6b4e95d3-37bc-4805-a079-29af10f99082">


## 개발 환경
local 환경에서 진행하였고
mongoDB만 mongoDB Atlas에서 제공하는 무료 클라우드 저장소를 사용했습니다.

## 실행 방법
```
npm install
```
```
npm start
```
```
localhost:8080
```
> .env 사용으로 프로젝트 정상 구동을 위해 DB_URI :mongodb url과, DECODED_TOKEN : 임의의 token 값을 설정해주신후에 구동해주시기 바랍니다.!

## 기술 스택
* node express
* mongo db
* mongoose
* socket io
* jwt login 구현
  
## 주요 기능
* crud 구현
* 파일 업로드 구현
* 소켓 구현
* 로그인 구현
  
## api 명세
|api|method|endpoint(url)|parameter|설명|
|----|--|---|---|--|
|auth|put|localhost:8080/auth/signup|{email:string, name:string, password:string }| 회원가입 api |
|auth|post|localhost:8080/auth/login|{email:string, password:string }|로그인 api|
|auth|get|localhost:8080/auth/status||jwt token을 통해 확인된 id|
|auth|patch|localhost:8080/auth/status|{status, jwt Token}|상태 변경 api|
|feed|put|localhost:8080/post/:postId|queryParameter(:postId)| 해당 게시물(postId) 수정 
|feed|post|localhost:8080/post/:postId|queryParameter(:postId)|해당 게시물(postId) 생성|
|feed|get|localhost:8080/post/:postId|queryParameter(:postId)|해당 게시물(postId) 조회|
|feed|get|localhost:8080/posts||전체 게시물 조회|
|feed|delete|localhost:8080/post/:postId|queryParameter(:postId)|해당 게시물(postId) 삭제|

