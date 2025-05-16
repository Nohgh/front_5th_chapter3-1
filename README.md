
## 7주차 과제 체크포인트

### 기본 과제


# HARD

## 7주차 과제 체크포인트

### 기본과제

- [x] 총 11개의 파일, 115개의 단위 테스트를 무사히 작성하고 통과시킨다.

#### 질문

> Q. handlersUtils에 남긴 질문에 답변해주세요.

> Q. 테스트를 독립적으로 구동시키기 위해 작성했던 설정들을 소개해주세요.

### 심화 과제

- [ ] App 컴포넌트 적절한 단위의 컴포넌트, 훅, 유틸 함수로 분리했는가?
- 컴포넌트 분리는 못하였고, 훅만 분리하였습니다. (🥲)
- [x] 해당 모듈들에 대한 적절한 테스트를 5개 이상 작성했는가?
- useDialogManage, useToastManage 훅 테스트에서 5개의 테스트만 작성하였습니다.(🥲)

## 과제 셀프회고



---

##  기술적 성장  

###  테스트 도구 학습  
- `Vitest`, `@testing-library/react`가 제공하는 다양한 기능 익혔습니다.
  - `describe`, `it`, `expect`, `beforeEach`,  ...
  - `render`, `screen`, `waitFor`, `getByXXX`, `userEvent` , ...

###  API 모킹 경험  
- `msw`를 활용한 API 모킹을 학습하였습니다. 
- 테스트 환경에서도 실제 요청-응답처럼 처리 가능하다는 점을 배울 수 있었습니다.

###  다양한 시나리오 설계  
- 과제 외에도 내가 진행한 프로젝트에 적용할 수 있는 테스트를 생각해볼 수 있는 기회였습니다.

---

##  코드 품질에 대한 고민  
![image](https://github.com/user-attachments/assets/c1777dd5-c298-43b0-bee9-dd1650c1026d)

- `describe`를 활용해 테스트 목적을 명시적으로 표현하려고 노력하였습니다.
- 하지만 어떤 기준으로 묶는 것이 좋은지에 대한 고민이 생겼습니다.
  >  이 부분은 추가적으로 질문드리겠습니다!



- ### handlersUtils 설명
-createMockHandlers(initEvents) 함수 내부에서 let events로 상태를 캡슐화하여 테스트 간 상태 공유를 방지했습니다.

- setupMockHandlers(initEvents)를 통해 각 테스트 파일 혹은 테스트 케이스에서 초기 mock 데이터를 명시적으로 주입할 수 있도록 개선했습니다.

- 기존처럼 server.use(...)를 사용하되, 테스트 파일 또는 테스트 케이스에서 setupMockHandlers([])를 호출하여 각 테스트 실행 전에 새로운 상태 기반의 mock을 주입하도록 했습니다.
