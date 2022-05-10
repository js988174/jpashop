# jpashop
# 실전 스프링 부트와 JPA 활용1 - 웹 애플리케이션 개발 강의 1

## H2 DB 설정
H2 TCP 설정을 Spring boot와 연결하하는 과정이다.
주의사항: H2 1.4.200 버전부터 MVCC 옵션이 제거되어서
url에서 MVCC=true를 지워줘야 한다.
```
spring:
  datasource:
    url: jdbc:h2:tcp://localhost/~/jpashop
    username: sa
    password:
    driver-class-name: org.h2.Driver

  jpa:
    hibernate:
      ddl-auto: create
    properties:
      hibernate:
        #        show_sql: true
        format_sql: true

logging.level:
  org.hibernate.SQL: debug
#  org.hibernate.type: trace
```

