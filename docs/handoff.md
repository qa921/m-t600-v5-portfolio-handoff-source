# M-T600-V5 포트폴리오 인수인계 문서

- 작성일: 2026-09-15 (UTC)
- 작성 근거: 이 저장소의 소스 자료(`docs/evidence/`, `docs/voice/`) + Vercel 계정 상태 실측
- 핵심 원칙: 사이트 카피(`site/`)가 아니라 **`docs/evidence/`가 사실 관계의 진실 원천**이다. 이 저장소는 완성본이 아니라 소스 팩트와 prior-state 산출물의 모음이다.

## 1. 보이스 가이드 적용 기준

- 현행: `docs/voice/2025-02-voice-guide.md` (2025-02-18 승인)
- 폐기: `docs/voice/2023-08-brand-notes.md` (superseded) — 낡은 카피의 출처
- 규칙 요약: 평이하고 구체적인 문장 / 범위가 제한적이면 "contributed to", "worked with", "prototype" 사용 / 날짜 있는 근거가 측정치를 줄 때만 성과 기술 / 최상급, "global", "award-winning", "AI transformation", 근거 없는 커리어 총량 금지 / 라우트 URL 유지 / 간결한 캡션 선호

## 2. 이번 수정 브랜치: `fix/m-t600-v5-voice-evidence-copy`

기존 라우트 URL(`/work/harbor`, `/work/fieldnotes`, `/archive/2024`)은 모두 유지하면서 공개 카피와 링크만 근거에 맞게 정정했다.

- `site/index.html` — "award-winning global platforms used by millions", "AI transformation", "launched 12 products in 8 countries" 제거. 검증된 직함(파트타임 독립 디자이너/개발자, 2025-02-07 스튜디오 로스터)과 프로토타입 작업만 기술. 미확정 스피킹·커리어 총량은 "pending confirmation" 보류 문구로 처리.
- `site/work/harbor/index.html` — "live logistics command center", "cut dispatch time by 40%", "product lead and lead engineer", live 프로젝트 링크 제거. Coastline Cooperative용 클릭 가능 프로토타입(2024-11-18 납품, 2024-12-03 리뷰 완료)만 기술하고 프로덕션 상태·성과 수치는 미검증임을 명시. (이슈 #1)
- `site/work/fieldnotes/index.html` — 기존 카피가 대체로 적합했음. 근거(2025-01-14 README, 2025-01-21 데모 녹화)에 맞춰 MapLibre 실험과 데모 녹화 내용 보강. 프로토타입 프레이밍 유지.
- `site/archive/2024/index.html` — 검증된 링크(Northline Journal 기고)만 링크로 유지. broken 2건(Harbor launch notes, Residency dispatch), moved 1건(Common Thread), redirect·canonical 불명 1건(Local Tools)은 텍스트 + 보류 상태로 전환. 깨진 내부 링크 `/archive/2023` 제거. (이슈 #3)

## 3. 공개 가능 vs 확인 필요

### 공개 가능 (날짜 있는 근거 존재)

| 주장 | 근거 |
|---|---|
| Field Notes = Astro + Markdown 컬렉션 + MapLibre 실험의 개인 프로토타입 (공개 런칭 아님) | 2025-01-14, 2025-01-21 |
| Northline Journal 기고 "Mapping after the storm" (Rin Aoki 바이라인) | 2024-04-06, 레지스터 verified |
| Common Thread 팟캐스트 게스트 출연 (participatory mapping) | 2024-05-19, 페이지 이동·트랜스크립트 보관 |
| River Assembly 패널 참석 (키노트 아님) | 2024-07-02 |
| Lantern Studio 12주 인터페이스 디자인 계약, 컴포넌트 인벤토리·접근성 주석 납품 (스태프 직함 아님) | 2023-03-12 / 2023-06-30 |
| Civic Signals 90분 매핑 워크숍 1회 퍼실리테이션 (14명) | 2024-09-09 |
| 직함: 파트타임 독립 디자이너/개발자 | 2025-02-07 |

### 확인 필요 / 보류 (확정 전 게시 금지)

| 항목 | 상태 |
|---|---|
| Harbor 프로덕션 여부·40% 수치·리드 직함 | 근거는 프로토타입 + 리뷰 완료뿐. 40%는 목표 슬라이드 출처. 이슈 #1 |
| 스피킹 초청 2건 | 확정 대기 중, 출연으로 게시 금지. 이슈 #2 |
| 수상 표현, "global", 커리어 총량(12 products/8 countries) | 근거 없음. 바이오 폼에 학위·수상·고용주 주장 없음 |
| Night Index | 공개 권한 기록 없음 (클라이언트/릴리스 없는 탐구 작업) |
| Open Transit | 쇼트리스트 컨셉뿐, 계약서 공란 |
| 아카이브 외부 링크 9건 중 verified 2건 외 | broken 2, moved 1, redirect 1, unverified 2, 권한 미상 1. 이슈 #3. `/archive/2024` 라우트는 유지하되 미검증 목적지를 canonical로 표현 금지 |

## 4. PR · 릴리스 흐름

- 릴리스 v0.8.0 (changelog상 2025-03-01): 정적 라우트 리프레시만. 주장 검증·아카이브 시정은 의도적 미완료.
- Draft PR #4 (`chore/m-t600-v5-archive-link-audit`): 참고용 감사 노트. **완료본 아님.** canonical 아카이브 URL·권한 확인·공개 카피 미해결 상태로 둠.
- 오픈 이슈: #1 Harbor 프로덕션 상태 / #2 미공개 이력 / #3 아카이브 링크.
- 본 수정은 별도 리뷰용 PR로 제출 (이 브랜치).

## 5. Vercel 상태 및 배포 차단 사유

- 프로젝트: `m-t600-v5-portfolio-handoff` (`prj_RBYbVeiL5UxsKUDAKc8EbbdojOoh`), 팀 `agent51-testing` (Hobby 플랜)
- 현재 배포 0건, 프로덕션 도메인/에일리어스 없음. 빌드 설정: `npm install` → `npm run build` → `dist/`, Node 24.x (저장소 `engines: node >= 20`과 호환)
- 빌드 스크립트 `scripts/build.mjs`는 `site/` → `dist/` 단순 복사이므로 로컬 검증은 Node ≥20에서 `npm run build` 한 줄이면 된다.

### 차단 사유 (2026-09-15 05:50 UTC, git 기반·파일 기반 배포 모두 시도)

1. **즉시 차단 — 일일 배포 할당량 소진**: HTTP 402 `payment_required`, 코드 `api-deployments-free-per-day` (100건/일, remaining 0). 리셋: **2026-09-16 약 05:52 UTC**. git 기반과 파일 업로드 기반 어느 쪽이든 배포 생성 자체가 불가.
2. **잠재 차단 — GitHub 연동 끊김**: 이 Vercel 계정에는 GitHub 계정이 연결되어 있지 않다. 같은 팀의 다른 프로젝트 git 트리거 배포들이 `errorCode: git_info_fail` / "A Github account is not connected to this Vercel account"로 실패 중이며, 할당량이 복구되어도 이 저장소의 푸시 기반 자동 배포는 같은 이유로 실패할 가능성이 높다.

### 대안

1. 할당량 리셋 후 재시도:
   - git 기반: `POST /v13/deployments` — `{ "name": "m-t600-v5-portfolio-handoff", "gitSource": { "type": "github", "repoId": "1370958855", "ref": "fix/m-t600-v5-voice-evidence-copy" } }`
   - 파일 기반: `site/`, `package.json`, `scripts/build.mjs`를 `files[]`로 업로드하면 Vercel이 `npm run build`를 실행해 `dist/`를 서빙 (git 연동 없이 PR 내용 프리뷰 가능)
2. Vercel 대시보드 → Connected Accounts / GitHub App에서 GitHub 연결 복구 → 이후 푸시·PR 프리뷰 자동화
3. Vercel CLI `vercel deploy` (토큰 필요, 동일 일일 할당량 적용)
4. 머지 전 검증은 로컬 `npm run build`로 대체 가능

## 6. 다음 담당자 액션 우선순위

1. 본 PR 리뷰·머지 → 할당량 리셋(2026-09-16 05:52 UTC경) 후 배포 재시도
2. 이슈 #1 해결 전까지 Harbor의 "live"·성과 수치 게시 금지
3. 이슈 #2: 스피킹 등 미확정 이력 확정 전 게시 금지
4. 이슈 #3: `docs/evidence/archive-link-register.csv` 기준으로 링크 복구/제거 (draft PR #4는 참고만)
5. 누락 파일 `docs/evidence/source-register.csv` 복구 또는 `projects-and-collaborations.md`의 참조 삭제
6. Vercel–GitHub 연동 복구
