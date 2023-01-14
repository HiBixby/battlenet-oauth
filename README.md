# Battlenet oauth

<div>
<img src="https://img.shields.io/badge/Battle.net-148EFF?style=flat-square&logo=Battle.net&logoColor=white" />
<img src="https://img.shields.io/badge/Spring Security-6DB33F?style=flat-square&logo=Spring%20Security&logoColor=white" />
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat-square&logo=Spring%20Boot&logoColor=white" />
</div>

* Battle.net의 oauth2 로그인 구현 예정

#### application.yml

```yml
Spring:
  security:
    oauth2:
      client:
        registration:
          battlenet:
            client-id: #발급받은 클라이언트 아이디
            client-secret: #발급받은 클라이언트 시크릿
            redirect-uri: http://localhost:8080/login/oauth2/code/battlenet
            authorization-grant-type: authorization_code
            scope: openid
            client-name: Battle.net
        provider:
          battlenet:
            authorization-uri: https://oauth.battle.net/authorize
            token-uri: https://oauth.battle.net/token
            user-info-uri: https://oauth.battle.net/oauth/userinfo
            jwk-set-uri: https://oauth.battle.net/jwks/certs
```
