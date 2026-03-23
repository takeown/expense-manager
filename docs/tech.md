# Tech

## 현재 스택
- Frontend: Next.js 16 App Router
- Language: TypeScript
- UI Styling: Tailwind CSS v4
- Lint: ESLint with `next/core-web-vitals` and TypeScript rules

## 현재 구현 기준
- 초기 단계에서는 서버 기능보다 프론트 흐름 검증을 우선한다
- 우선 `mock data`로 화면과 사용자 흐름을 만든다
- 폴더 구조는 `app/` 중심으로 단순하게 유지한다

## 추천 다음 선택
### Database
- 추천: Supabase PostgreSQL
- 이유: 개인 프로젝트 MVP에 충분하고, 이후 인증과 스토리지까지 확장하기 쉽다

### Auth
- 1차: 인증 없이 단일 사용자 흐름부터 구현
- 2차: 필요 시 Supabase Auth 추가

### Deployment
- 추천: Vercel
- 이유: Next.js 배포가 가장 단순하고 초기 운영 부담이 적다

## 데이터 접근 단계
1. mock data
2. local persistence 또는 서버 액션 연결
3. Supabase 스키마 확정
4. AI 분석 및 리포트 연결

## 주의사항
- `.env*` 파일은 커밋하지 않는다
- 금융 데이터 예시는 익명화한다
- 원본 거래 텍스트 저장은 최소화한다
