# overwatch-rank-recorder

battle.net oauth2 login을 구현할 예정

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
            client-name: Battlenet
        provider:
          battlenet:
            authorization-uri: https://oauth.battle.net/authorize
            token-uri: https://oauth.battle.net/token
            user-info-uri: https://oauth.battle.net/oauth/userinfo
            user-name-attribute: id
            jwk-set-uri: https://oauth.battle.net/jwks/certs
```
