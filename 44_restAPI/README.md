# REST API

- REST는 HTTP를 기반으로 클라이언트가 서버의 리소스에 접근하는 방식을 규정한 아키텍처이다.
- REST API는 REST를 기반으로 서비스 API를 구현한 것을 의미한다.
- REST의 기본원칙을 성실히 지킨 서비스 디자인을 RESTful 이라고 표현한다.

## REST API 의 구성

| 구성요소               | 내용                           | 표현방법        |
| ---------------------- | ------------------------------ | --------------- |
| 자원(resource)         | 자원                           | URL(엔드포인트) |
| 행위(verb)             | 자원에 대한 행위               | HTTP 요청메서드 |
| 표현 (representations) | 자원에 대한 행위의 구체적 내용 | 페이로드        |

## REST API 설계 원칙

| HTTP 요청 메서드 | 종류           | 목적                  | 페이로드 |
| ---------------- | -------------- | --------------------- | -------- |
| GET              | index/retrieve | 모든/특정 리소스 취득 | X        |
| POST             | create         | 리소스 생성           | O        |
| PUT              | replace        | 리소스 전체 교체      | O        |
| PATCH            | modify         | 리소스의 일부 수정    | O        |
| DELETE           | delete         | 모든/특정 리소스 삭제 | X        |

- 리소스에 대한 행위는 HTTP 요청 메서드를 통해 표현하며 URI에 표현하지 않는다.

```
# bad
GET /todos/delete/1

# good
DELETE /todos/1
```

## 이후는 실습에 관한 내용이므로 다른 자료로 대체하려고 한다.
- 시간적 여유가 있다면 하단의 영상은 꼭 보는것을 추천한다.
- https://tv.naver.com/v/2292653

- REST는 하나의 디자인 아키텍처라고 책에서도 설명하고있다.
- REST는 REpresentational State Transfer 의 약자이다.
- REST는 아키텍처 스타일이다.
- 아키텍처 스타일이란 제약조건의 집합이다.

## ETC
- GET 요청시 parameter를 body로 받는 것은 RESTful한 설계가 아니다.
- DELETE API의 경우 params 로 삭제 타겟을 지정하는 경우도 있다.
- RESTful한 API가 중요하다고 생각된다. 하지만 모든 상황에서 그러한 적용이 힘들다고도 생각된다.
- 실제 개발 시 각 상황에 맞게 유연한 적용도 필요하다고 생각된다.