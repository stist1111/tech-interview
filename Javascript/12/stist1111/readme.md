## Question 12. same-origin policy란?

`동일 출처 정책` (same-origin policy)은 어떤 출처(origin)에서 불러온 문서나 스크립트가 다른 출처에서 가져온 리소스와 상호작용하는 것을 제한하는 중요한 보안 방식입니다.

### 동일한 출처란 ?

두 URL의 프로토콜, 포트(명시한 경우), 호스트가 모두 같아야 동일한 출처라고 말합니다.

### 프로토콜, 포트, 호스트를 확인하는 방법은?

현재 페이지의 프로토콜과 호스트, 포트를 확인하는 방법은 간단하다.
개발자 도구를 열고 `location`을 입력해보면 host, port, protocol 정보를 확인할 수 있다.

### 그렇다면 출처가 다른 URL에 리소스를 요청하려면 어떻게 해야할까?

출처가 다른 URL에서 리소스를 요청하게 되면 동일 출처 정책에 의해 에러가 발생하는데,
이를 해결 하기 위해서 `CORS`(Cross-Origin Resource Sharing) 정책이 등장하였다.

### CORS란?

교차 출처 리소스 공유(Cross-Origin Resource Sharing, CORS)는 추가 HTTP 헤더를 사용하여, 한 출처에서 실행 중인 웹 애플리케이션이 다른 출처의 선택한 자원에 접근할 수 있는 권한을 부여하도록 브라우저에 알려주는 체제입니다. 웹 애플리케이션은 리소스가 자신의 출처(도메인, 프로토콜, 포트)와 다를 때 교차 출처 HTTP 요청을 실행합니다.

서버 단 해결방법

1. Access-Control-Allow-Origin response header 추가 방법
2. Node.js Express 미들웨어 CORS

클라이언트 단 해결방법

1. proxy 설정

CORS의 사용 방법은 [yejinh님의 블로그](https://velog.io/@yejinh/CORS-4tk536f0db)를 참고하자.

##### 출처

[MDN - 동일출처정책](https://developer.mozilla.org/ko/docs/Web/Security/Same-origin_policy)
[MDN - CORS](https://developer.mozilla.org/ko/docs/Web/HTTP/CORS)
[yejinh님의 블로그](https://velog.io/@yejinh/CORS-4tk536f0db)
