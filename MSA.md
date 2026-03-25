MSA 강의 1독 완료
Spring Cloud로 개발하는 마이크로서비스 애플리케이션(MSA)
3. 소프트웨어 아키텍처
7. Monolithic vs. Microservice
8. Microservice Architecture의 이해
- 1.팀단위로 작업할 경우 인터페이스를 제공해야한다.(아마존ceo-20년전 메일 내용 핵심)
- Monolith Props 장점 : 쉽고 빠른 소스 코드 구현, 쉬운 디버깅, 쉬운 배포 ||| 단점 : 의존관계 강함, 기술의 제안, 큰 단위, 기술의 제안이 있음
- Microservice Props 장점: 작은 단위, 의존관계 약함, 기수르이 제안이 없음 ||| 단점 : 네트워크 지연 시간 늘어남, 데이터의 일관성을 유지하기 어려움, 코드구현의 어려움
9. SOA vs. MSA
   SOA : 비즈니스 측면에서의 서비스 재사용성 - 재사용을 통한 비용 절감
   MSA : 서비스 간의 결합도를 낮추어 변화에 능동적으로 대응
        - 각 독립된 서비스가 노출된 REST API를 사용

10. Microservice Architecture Structures ➀
   1. MSA의 특징
      1) 작은 서비스
      2) 독립된 서비스
   2. 독립된 서비스
      1) 독립적 실행
      2) 구현, 배포 실행, 장애에 대한 영향 받지 않음
      ex) 어떠한 서비스에 문제가 생겨도 이과 관계없는 서비스에는 기능이 가능해야한다.
   3. 응집된 서비스
      1) 하나의 서비스는 기능적으로 응집
      2) 서비스의 역할이 한 가지 일을 위해 묶여야 함 -> 단준 명확, 오류 최소화
      ex) 수강 신청 시스템
   4. Microservice 기획
      - 소로 다른 서비스의 디비가 같은 스키마를 필요로 할때 스키마를 공유하는게 아니라 각각의 디비에 스키마를 가지고 있고 MessageQueue를 (발행 -> Queue -> 구독) 다른 디비로 업데이트 해준다.
   <img width="2114" height="1185" alt="image" src="https://github.com/user-attachments/assets/48b2e691-b768-4883-a0f3-7bd31597e9a3" />
  5. Service Decomposition
     <img width="2112" height="1251" alt="image" src="https://github.com/user-attachments/assets/baecbc37-f61a-4c40-bd39-2c71df89174a" />

  6. Polyglot Persistence
     <img width="2087" height="1233" alt="image" src="https://github.com/user-attachments/assets/0d3a03e2-41aa-492b-a7cc-0f99e34e5c7f" />

11. Microservice Architecture Structures ➁
    1. Service Mesh -> Network
       - Service Discovery : 언제 서비스가 만들어졌고 그러한 서비스가 어디에 위치하고 있으며 해당하는 서비스를 호출하기 위해서 어떠한 방법을 선택해야 되는지 등등 이런 것들을 관리하는 것을 서비스 디스커버리
       - Config.Store : 다음 각각의 마이크로서비스를 사용함에 있어서 환경 구성 정보가 필요하다고 하면 외부에 있는 스토리지를 별도로 사용해 줌으로써 각각의 마이크로서비스는 환경이라든가 어떠한 설정 정보를 변경함에 있어서 다시 배포하지 않도록 도와줄 수 있도록 우리는 Configuration 서비스를 외부에 두어서 사용
       - Service Router
       - LoadBalancing
   <img width="2112" height="1181" alt="image" src="https://github.com/user-attachments/assets/d62e9ac0-5383-429a-a1d0-e9103ee1a95e" />

   2. Service Mesh Capabilities
   <img width="2113" height="1184" alt="image" src="https://github.com/user-attachments/assets/2697d81a-de04-42fd-83be-f9e014337f17" />

   3. RESTful Web Service - Rest api를 사용함으로써 강력한 규칙을 적용해야한다.
      - level3: 다음에 어떠한 동작을 해야하는지 정보를 얻을수 있다.
      <img width="2118" height="1190" alt="image" src="https://github.com/user-attachments/assets/bdb0859c-939e-49dc-9558-b8c7f05df04c" />
   4. RESTful Web Service
      
   <img width="2127" height="1205" alt="image" src="https://github.com/user-attachments/assets/f3612d79-3a35-45ea-80a5-a7b58b128b82" />


































