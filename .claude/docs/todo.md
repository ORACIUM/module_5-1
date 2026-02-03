# Project TODO List

## Feature: 로그인/회원가입 (Authentication)

### Phase 1: Database (DB)
- [ ] User 모델 생성
  - [ ] 테이블 설계 (id, email, username, password_hash, created_at, updated_at)
  - [ ] SQLAlchemy 모델 정의 (`backend/app/models/user.py`)
  - [ ] 고유 제약조건 설정 (email, username unique)
- [ ] User CRUD 함수 작성
  - [ ] 사용자 생성 (create_user)
  - [ ] 이메일로 사용자 조회 (get_user_by_email)
  - [ ] 사용자명으로 사용자 조회 (get_user_by_username)
  - [ ] ID로 사용자 조회 (get_user_by_id)
- [ ] 데이터베이스 테스트 작성
  - [ ] User 모델 제약조건 테스트
  - [ ] CRUD 함수 테스트

### Phase 2: Backend (BE)
- [ ] Pydantic 스키마 정의
  - [ ] UserCreate (회원가입 요청)
  - [ ] UserLogin (로그인 요청)
  - [ ] UserResponse (사용자 정보 응답)
  - [ ] Token (토큰 응답)
- [ ] 인증 유틸리티 구현
  - [ ] 비밀번호 해싱 함수
  - [ ] 비밀번호 검증 함수
  - [ ] JWT 토큰 생성 함수
  - [ ] JWT 토큰 검증 함수
- [ ] 인증 API 엔드포인트 작성
  - [ ] POST /api/auth/register (회원가입)
  - [ ] POST /api/auth/login (로그인)
  - [ ] GET /api/auth/me (현재 사용자 정보)
  - [ ] POST /api/auth/logout (로그아웃 - 선택사항)
- [ ] 인증 미들웨어/의존성 구현
  - [ ] get_current_user 의존성 함수
  - [ ] 토큰 검증 로직
- [ ] API 테스트 작성
  - [ ] 회원가입 API 테스트
  - [ ] 로그인 API 테스트
  - [ ] 인증이 필요한 엔드포인트 테스트

### Phase 3: Frontend (FE)
- [ ] 페이지 생성
  - [ ] 로그인 페이지 (`/login`)
  - [ ] 회원가입 페이지 (`/register`)
- [ ] 컴포넌트 작성
  - [ ] LoginForm 컴포넌트
  - [ ] RegisterForm 컴포넌트
  - [ ] 폼 유효성 검사 로직
- [ ] API 연동
  - [ ] 회원가입 API 호출 함수
  - [ ] 로그인 API 호출 함수
  - [ ] 사용자 정보 조회 API 호출 함수
- [ ] 인증 상태 관리
  - [ ] 토큰 저장 (localStorage/cookies)
  - [ ] 로그인 상태 Context/Provider
  - [ ] Protected Route 구현
- [ ] UI/UX 개선
  - [ ] 로딩 상태 표시
  - [ ] 에러 메시지 표시
  - [ ] 성공 메시지 및 리다이렉션
- [ ] 컴포넌트 테스트 작성
  - [ ] LoginForm 렌더링 테스트
  - [ ] RegisterForm 렌더링 테스트
  - [ ] 폼 제출 인터랙션 테스트

---

## 작업 순서
1. **DB 작업 완료** → 2. **BE 작업 완료** → 3. **FE 작업 완료**

각 Phase는 순차적으로 진행하며, 이전 단계가 완료된 후 다음 단계로 진행합니다.
