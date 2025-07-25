# 프로젝트 협업 규칙

## 브랜치 전략
브랜치 명은 크게 세 부분으로 나누어 구분하기
- 처음엔 프론트엔드(Front-End)와 백엔드(Back-End) 작업을 명확히 구분하기 위해 브랜치 이름에 `fe`, `be` 접두사를 사용하기
- 중간에는 라벨명 표기
- 마지막엔 issue의 넘버 표기

### 예시  
- `fe/enhancement/23`  
- `be/maintenance/34`

---

## Git Issue 활용 방식

Git Issue는 **프로젝트 완성을 위해 개발자가 수행해야 하는 기능 단위 작업을 세분화**해서 관리하기

- 자신이 맡은 기능을 **기능 단위로 쪼개어 Issue 등록**
- Issue 제목은 간결하게, 내용은 구체적으로 작성
- 할당(Assignee), 라벨(Labels), 유형(Type) 등을 활용해 업무 분류

### 예시

- **제목:** [BE] 유저 로그인 API 구현
- **내용:**
  - 개요: 서용자 인증 정보 검증 및 인증 토큰 발행
  - 작업 내용:
    - [ ] JWT 발행
    - [ ] 컨트롤러 구현
    - [ ] 서비스 구현

---

## 커밋 메시지 작성 규칙

### 커밋 메시지 구조

> 헤더, 본문은 빈 행으로 구분한다.

```
[개발 분야] 타입: 제목

본문
```

1. 제목은 50글자 이내로 작성한다.
2. 제목, 본문의 첫 글자가 영문일 경우 대문자로 작성한다.
3. 제목, 본문 둘 다 마침표를 사용하지 않는다.
4. 본문의 각 행은 72글자 이내로 작성한다.
5. 제목은 뭘 했는지, 본문은 왜 or 기대 효과를 간결하게 적는다.
6. 개발 분야는 `BE` 혹은 `FE` 라고 표기한다.
7. 타입은 아래의 표를 참고하여 작성한다.

| 타입 이름    | 설명                                      |
|-------------|-------------------------------------------|
| feat        | 새로운 기능에 대한 커밋                     |
| fix         | 버그 수정에 대한 커밋                       |
| build       | 빌드 관련 파일 수정 / 모듈 설치 또는 삭제    |
| chore       | 그 외 자잘한 수정에 대한 커밋               |
| ci          | CI 관련 설정 수정에 대한 커밋               |
| docs        | 문서 수정에 대한 커밋                       |
| style       | 코드 스타일 혹은 포맷 등에 관한 커밋         |
| refactor    | 코드 리팩토링에 대한 커밋                   |
| test        | 테스트 코드 수정에 대한 커밋                |
| perf        | 성능 개선에 대한 커밋                       |

### 예시

`[BE] feat: Projects 생성 API 작성`

```
[BE] refactor: For문 코드 stream으로 변경

* Stream을 통한 코드 간결화
* 체이닝 방식을 통한 가독성 향상
```