# SpringBoot-Web
### [VELOG](https://velog.io/@hye_b/series/SpringBoot%EC%99%80-AWS%EB%A1%9C-%ED%98%BC%EC%9E%90-%EA%B5%AC%ED%98%84%ED%95%98%EB%8A%94-%EC%9B%B9-%EC%84%9C%EB%B9%84%EC%8A%A4)
## - 교재 


<img src="https://t1.daumcdn.net/cfile/tistory/994D4A415DE2738514" width="400" height="600">

**스프링 부트와 AWS로 혼자 구현하는 웹 서비스 - 이동욱 지음**      


## 개발환경
 

| - |버전|
|---|---|
|운영체제|Window 10|
|개발 툴|IntelliJ IDEA 2021.1|
|JDK|JDK 14|
|Gradle|6.7.1|
        * Gradle version downgrade
        p.74 http://bit.ly/382Q7d7 
        * Gradle version upgrade 
        https://jojoldu.tistory.com/539
        
<details>
<summary> DAY 1 </summary>

- **Intellij로 프로젝트 만들기**
    - gradle project에서 springboot project로 변경하기 
- **Test code 작성하기**
    - TDD : 테스트가 주도하는 개발, 테스트 코드를 먼저 작성
        1. RED : 항상 실패하는 테스트 작성
        2. GREEN : 테스트가 통과하는 프로덕션 코드를 작성
        3. REFACTOR : 테스트가 통과하면 프로덕션 코드를 리팩토링 합니다.
    - 단위테스트 : 기능 단위의 테스트 코드를 작성

- **Test code를 작성해야하는 이유**
    - 단위 테스트는 **개발 단계 초기에 문제를 발견**
    - 단위 테스트는 개발자가 나중에 코드를 리팩토링하거나 라이브러리 업그레이드 등에서 **기존 기능이 올바르게 작동하는지 확인 가능** ex)회귀 테스트
    - 단위테스트 **기능에 대한 불확실성을 감소**
    - 단위테스트는 시스템에 대한 **실제 문서를 제공**, 단위 테스트 자체가 문서로 사용 가능 
- **Test code 작성 프레임워크**
    - xUnit , java => JUnit 

- **@SpringBootApplication**
    - 스프링 부트의 자동 설정, 스프링 Bean읽기와 생성 모두 자동으로 설정 
    - 시작 위치부터 설정을 읽어 가지 때문에 프로젝트의 최상단에 위치 
    - SpringApplication.run => 내장 WAS실행  
    
      => '언제 어디서나 같은 환경에서 스트링 부트를 배포' 
      
      => 서버에 톰캣을 설치할 필요가 없고 스프링 부트로 만들어진 JAR로 실행 
      </details>
      
<details>
<summary> DAY 2 </summary>

- ### 관계형 DB를 이용하는 project에서 OOP 문제점
    1. 관계형 데이터베이스는 SQL만 인식 -> **단순 반복 작업 문제** 
    2. **패러다임 불일치**

    =>  위의 문제 해결  **ORM**   


- **JPA(Java Persistence API)** : 자바 표준 ORM , 인터페이스의 모음

- **Spring Data JPA** : Spring에서 JPA 사용시 구현체를 직접 다루지 않고 사용하는 모듈  
                    
                    JPA <- Hibernate <- Spring Data JPA

- ##  요구사항 분석 

    - 게시판 
        - 게시글 조회
        - 게시글 등록
        - 게시글 수정
        - 게시글 삭제
        
    - 회원
        - 구글 / 네이버 로그인
        - 로그인한 사용자글 작성 권한
        - 본인 작성 글에 대한 권한 관리     

- SpringDataJpa Test 코드 작성 
- 수정,등록,조회 API 만들기 
    - Request 데이터를 받을 Dto
    - API 요청을 받을 Controller/
    - 트랜잭션, 도메인 기능 간의 순서를 보장하는 Service
- 수정 API만들기에서 PostApiControllerTest Test 

</details>

<details>
<summary> DAY 3 </summary>


- 조회 API 만들기
- JPA Auditing으로 생성/수정 시간 자동화 

</details>


