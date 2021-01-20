## Question 12. same-origin policy에 대하여

우선 오리진 (origin) 이란 프로토콜 + 호스트 + 포트로 구성된 주소를 의미한다. (하위 경로는 오리진에 포함하지 않는다.)

### Ex 1. 도메인과 오리진의 차이

도메인 : naver.com  
오리진 : https://www.naver.com/80

### Ex 2. 이 둘은 같은 오리진! (하위 경로만 다르므로)

오리진 1 : https://newsstand.naver.com/?list=ct1  
오리진 2 : https://newsstand.naver.com/?list=ct2

동일 출처 정책 (same-origin policy)은 보안 상 어떤 오리진에서 다른 오리진의 리소스에 접근하는 것을 제한하는 브라우저의 규칙입니다.

## 추가 질문 : 그럼 어떻게 다른 오리진의 리소스를 불러올 수 있나요?

다른 오리진간 리소스를 주고받기 위해서 Cross-Origin Resource Sharing(CORS) 정책이 등장했습니다.

## CORS란?

CORS는 서버에서 전송하는 HTTP 헤더를 통해 특정 호스트에 액세스 권한을 부여하는 방법입니다.  
HTTP 헤더에 `Access-Control-Allow-Origin` 키와 액세스를 허용할 호스트를 값으로 부여하면 해당 호스트가 다른 오리진이더라도 접근할 수 있게 됩니다.

다만 IE 10 아래 버전에서는 지원하지 않으며, 하위 브라우저의 호환을 위해서는 `JSONP` 라는 방법을 사용해야 합니다.  
하지만 JSONP는 GET 메서드만을 지원하고, 보안상의 이슈로 CORS를 사용하는 것이 권장됩니다.
