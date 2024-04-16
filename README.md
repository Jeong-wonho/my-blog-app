# My-blog-app

## 프로젝트 소개
express 학습을 위한 개인 프로젝트 입니다. 간단한 강의를 참고하여 블로그를 제작해보았습니다.
이미지 추가

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
## 기술 스택
* node express
* mongo db
* mongoose
* File upload
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

