## My Chatting App with Vanilla JS

## 기능

*대화명에 원하는 이름 지정
*ngrok을 통해 주소 생성 후 다른 네트워크에서 상대방과 채팅 가능

## 소개

- 목표: 바닐라 자바스크립트와 소켓 IO라이브러리를 사용해서 간단한 채팅 앱 만들기

- 방식: 채팅을 서버에 날리면 서버가 다른 사용자에게 전달하는 처리

- 이용 기술

  - node js: 서버로 채팅을 보내고 그 것을 처리해서 client로 보내주는 역할 (express)

  - socket.io: npm download

  - vanilla javascript: chatting을 동적으로 넣어주고 표현하기 위함

  - Flex-box: layout 구현

  - ngrok: 외부에서 다른 사용자가 접속하여 함께 채팅 가능

## 유용한 기능 및 도움받은 기능

es6) Destructing Assignment
es6) Shortand Property Names

## 실행 방법

```
$ git clone https://github.com/shseok/chattingWithJS.git
$ cd .\chattingWithJS\
$ npm install
$ npm start (nodemon 실행)
```

만약 ngrok을 실행하고 싶다면 다른 터미널에서 server에서 받은 port 번호를 입력 👇

```
$ngrok http (port number)
```

## 실행 과정

```
1. npm init -y : package.json 생성

- package.json - app의 manifest file

2. npm install express socket.io moment

3. npm install -g nodemon : js file의 변경이 있을 때마다 자동으로 실행(적용)

이후 node app.js -> nodemon app.js (server listening ...) - only app.js listening

4. emit을 통해 clinet와 server가 메시지를 주고 socket.on의 data로 메시지를 받는다.

5. client에서 받은 메세지를 처리

6. html, css (hard coding)뼈대 작성 - UI용

7. client (chat.js)의 li 생성 부분 수정

8. npm install -g ngrok
   ngrok은 내가 가진 컴퓨터를 외부사람이 접속할 수 있도록 한다.(test용)
   실행방법 : app.js실행 후 port 확인 -> ngrok http (port번호) -> forwarding address (외부 접속용 주소)
```

## 주의사항

html파일에서 socket.io.js가 있는 경로를 찾지 못 할 경우 cndjs.com에서 socket.io 경로를 copy 후 사용

## 보완해야할 부분

1. 사진 바뀜 현상
2. 빈 칸 입력시 칸의 형태 변형

## 참고 사이트 (ref)

https://cdnjs.com/
https://www.nextree.co.kr/p8468/
