# 이력서

---

**김선종**

**백엔드 개발자**  
커뮤니케이션을 중시하는 백엔드 개발자입니다. 개발자는 코딩 실력뿐만 아니라 다양한 사람들과 협업하는 것이 중요하다고 생각합니다. 커뮤니케이션의 중요성을 알고 함께 일하고 싶은 개발자를 목표로 하고 있습니다.

- **이름:** 김선종
- **Email:** rlatjswhd8200@gmail.com
- **Github:** [https://github.com/sunjong0214](https://github.com/sunjong0214)
- **Blog:** [https://sunjong0214.github.io](https://sunjong0214.github.io)

---

### 자기 개발 활동

#### [기술 블로그 운영](https://sunjong0214.github.io)
- 23/12월부터 꾸준히 글 작성
- 공부한 내용 정리 및 복습 위주
 
#### [알고리즘 스터디](https://github.com/won-and-jong/Data-Structures-and-Algorithms)
- 자료구조 위주의 알고리즘 스터디 진행
- 스터디원들과 코드 리뷰를 통해 피드백
---

### 사용 기술

#### Backend
- **언어:** Java
- **프레임워크:** Spring, Spring Boot
- **데이터베이스:** MySQL, H2
- **ORM:** Spring Data JPA, Mybatis, QueryDSL

#### 협업 도구
- **이슈 관리:** Github
- **디자인 협업:** Figma
- **버전 관리:** Git
- **커뮤니케이션:** Slack, Notion

---

### 프로젝트

#### [WalkiePaw](https://github.com/WalkiePaw/walkie-paw)
- **기간:** 2024.06 ~ 현재
- **소개:** 반려견 산책 매칭 서비스로, 매칭된 회원들 간 채팅을 통해 서로 협의하는 웹사이트입니다.
- **사용 기술:** Spring Data JPA, Querydsl, Rest API 설계, MySQL, WebSocket, STOMP, AWS S3
- **역할:** 
  - `페이징 중복 코드 제거`
    - Pagination Slice<> 사용 시 다음 페이지 있는지 확인 중복 코드 발생
    - QuerydslRepositorySupport을 커스텀한 클래스 구현해 중복 코드 제거
  - `JPA Entity 설계 및 도메인 모델 패턴 적용`
    - Entity와 관련된 비즈니스 로직이 여기저 흩어져있는 문제
    - Entity와 관련된 로직은 Entity 안에 두어 좀더 객체지향적 설계 적용 -> 메서드 재사용성 높아짐
  - `Spring Data JPA 단점 보완`
    - Spring Data JPA는 동적 쿼리나 복잡한 쿼리 작성시 어려움
    - Querydsl 라이브러리 사용해 동적쿼리 및 복잡한 쿼리 처리
  - `실행 시간 로깅 AOP 구현`
    - 게시글 요청시 성능 이슈가 발생 -> 어디서 병목이 발생하는지 찾기 힘듬
    - @Trace 어노테이션을 통해 실행 시간을 체크하는 logging AOP 구현
  - `Spring WebSocket & STOMP를 이용해 1:1 채팅 구현`
  - `게시글 좋아요 수 스케줄러를 통해 최적화`
    - 게시글 좋아요 누를시 동시에 많은 요청이 오면 성능에 문제가 발생할 수 있음(조인이 포함된 쿼리가 여러번 나감)
    - 성능 향상을 위해 게시글의 좋아요 수를 카운트하는 것은 스케줄러를 통해 특정 시간마다 update 하게 수정
      -> 좋아요 수는 데이터의 정합성이 중요하기 보단 대략적인 수를 체크하고 사용자가 나중에 게시글을 쉽게 찾기 위한 장치이기 때문
  - `JPA N + 1 문제 해결`
    - 게시글 조회시 게시글 사진을 가져오는 쿼리 나가는 문제
    - batch_size를 설정해 연관된 사진을 in 절을 통해 한번에 가져오게 수정 (3s -> 1s 단축)
  - `AWS S3, RDS 사용`
    - 게시글, 회원 이미지 업로드에 S3 사용
    - RDS 사용해 DB 구축

#### [MOS](https://github.com/bitcamp-teams/mos)
- **기간:** 2024.04 ~ 2024.05
- **소개:** 스터디 그룹을 모집하고, 스터디 활동 결과물인 나무위키 형식의 문서를 작성하여 참여자들의 포트폴리오로 활용할 수 있는 웹사이트입니다.
- **역할:**
  - OAuth2 활용 소셜 로그인
  - Mybatis 환경에서 Pageable 인터페이스 활용해 Pagination
  - Spring MVC 기반 개발
  - Spring Interceptor 이용 로그인 확인 처리
  - Argument Resolver를 이용해 로그인 유저 공통 코드 처리
  - NCP Object Storage를 이용한 사진 업로드
- **사용 기술:** Spring MVC, Mybatis, Thymeleaf, NCP, MySQL

#### **42 Seoul La Piscine** (2023.02 ~ 2023.03)
  - C언어 이용해 과제 해결
  - 과제 제출 시 구성원들끼리 코드 리뷰 후에 제출 가능 → 리뷰 문화 경험
    
#### **(디지털컨버전스) 파이썬 & 자바기반 빅데이터 SW개발자 양성 B** (2022-06 ~ 2022~12)
  - 스프링 기반 프로젝트 경험
  - CRUD 위주의 클론 코딩 프로젝트
---

### 활동

- **서울형 뉴딜 일자리 연계 DevOps 30일 완성 AWS 웹 데브옵스 기반 교육 과정**  
  (2024.06 ~ 2024.07)

- **Bitcamp 네이버클라우드캠프 데브옵스 5기**  
  (2023.11 ~ 2024.05)

- **42 Seoul La Piscine**  
  (2023.02 ~ 2023.03)

- **(디지털컨버전스) 파이썬 & 자바기반 빅데이터 SW개발자 양성 B**
  (2022-06 ~ 2022~12)
  
---
