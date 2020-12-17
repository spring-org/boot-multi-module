# Spring Boot Multi Module Settings

- 멀티 모듈로 구성하는 이유
    - CORE, API, BATCH 와 같은 구조적으로 역할이 다른 모듈을 분리 및 관리하기 위함

- 모듈의 정의를 명확하여 구분
    - 일반적으로 큰 체계의 구성요소이고, 다른 구성요소와 독립적으로 운영이 가능한 기능의 집합

- Common
  - 순서 Java Class 만 정의
  - DTO, Util Class 만을 배치

- Domain
  - 서비스 비즈니스에 대한 로직이 없음
  - 저장소 외 시스템 특성을 알지 않아야 한다.
  - 도메인 모듈을 조합한 더 큰 단위의 도메인 모듈이 있을 수 있다.
  
- Core
  - 어플리케이션, 도메인 비즈니스로부터 독립적
  - filter, security, logging
  - 다른 시스템들간의 통신을 담당하는 모듈, 이벤트 처리 모듈

- Application
  - 배치, api 모듈

- 문제1
  - 데이터베이 커넥션
  
## 참고

- [(Gradle dependency) api와 implementation 차이](https://jongmin92.github.io/2019/05/09/Gradle/gradle-api-vs-implementation/)
