## 1. http와 https 차이점을 설명하세요.

## 2. 주소창에 url을 입력했을 때, 브라우저에 보여주기까지 어떤 동작이 일어나는지 설명하세요.

## 3. tcp의 특징과 udp의 특징을 설명하세요.

## 4. tcp와 udp의 차이점을 설명하세요.

## 5. tcp 연결과정을 설명하세요.

## 6. Cookie VS Session 이 무엇인지 설명하고 차이점을 설명하세요.

## 7. RESTful API에 대해 설명하세요.

## 8. CORS에 대해 설명하세요.

브라우저에서는 보안적인 이유로 cross-origin HTTP 요청들을 제한합니다. 그래서 cross-origin 요청을 하려면 서버의 동의가 필요합니다. 만약 서버가 동의한다면 브라우저에서는 요청을 허락하고, 동의하지 않는다면 브라우저에서 거절합니다.
이러한 허락을 구하고 거절하는 메커니즘을 HTTP-header를 이용해서 가능한데, 이를 CORS(Cross-Origin Resource Sharing)라고 부릅니다.

### 새끼 문제 8-1. cross-origin이란 무엇인가요?

cross-origin이란 프로토콜이 다르거나 도메인이 다르거나 포트번호가 다른 이 세가지 경우의 하나라도 해당할 경우를 말합니다.

### 새끼 문제 8-2. cors의 동작방식에 대해 설명하세요.

Simple requests인 경우, 서버로 요청을 한 후, 서버의 응답이 왔을 때 브라우저가 요청한 Origin과 응답한 헤더 Access-Control-Request-Headers의 값을 비교하여 유효한 요청이라면 리소스를 응답합니다. 만약 유효하지 않은 요청이라면 브라우저에서 이를 막고 에러가 발생합니다.
preflight 요청일 경우, Origin헤더에 현재 요청하는 origin과 Access-Control-Request-Method헤더에 요청하는 HTTP method와 Access-Control-Request-Headers요청 시 사용할 헤더를 OPTIONS 메서드로 서버로 요청합니다. 이때 내용물은 없이 헤더만 전송하는데, 브라우저가 서버에서 응답한 헤더를 보고 유효한 요청인지 확인합니다. 만약 유효하지 않은 요청이라면 요청은 중단되고 에러가 발생합니다. 만약 유효한 요청이라면 원래 요청으로 보내려던 요청을 다시 요청하여 리소스를 응답받습니다.

### 새끼 문제 8-3. simple requests와 prflight에 대해 설명하세요.

## 9. CSRF나 XSS공격을 막는 방법을 설명하세요.

먼저, CSRF 공격을 막기 위해서는 서버에서 CSRF Token을 생성하여 세션에 저장하고, 프론트엔드에서 요청 시 해당 Token을 함께 전송하여 인증하는 방법이 있습니다. 또한, SameSite 속성을 쿠키에 설정하여 도메인이 다른 사이트에서는 쿠키를 사용할 수 없도록 제한하는 방법도 있습니다.

XSS 공격을 막기 위해서는 입력 값들을 유효성 검증하고, 특수문자들을 제외하는 정규식을 통해서 제거합니다. 또한, 서버에서 CSP(Content-Security-Policy)정책을 설정하여, 허용된 스크립트만 실행되도록 제한 할 수도 있습니다. 마지막으로, HTTP 대신에 신뢰할 수 있는 HTTPS를 사용하여 통신 프로토콜을 암호화할 수 있습니다.
