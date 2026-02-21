# 가족 여행 플래너 AI — 오픈소스

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude.ai](https://img.shields.io/badge/Claude.ai-Projects-orange?logo=anthropic)](https://claude.ai)
[![Gemini](https://img.shields.io/badge/Gemini-Gems-blue?logo=google)](https://gemini.google.com)
[![한국어](https://img.shields.io/badge/언어-한국어-brightgreen)](README.md)

> 초등학생 자녀를 둔 부모를 위한 **AI 여행 플래너**입니다.
> 역사·교육 여행지 추천, 최적 동선, 아이 눈높이 설명, 저녁 퀴즈까지 한 번에 만들어 드립니다.

---

## 이런 분들께 딱 맞습니다

- 아이와 함께 **의미 있는 여행**을 하고 싶은 부모
- 여행지 조사에 시간을 너무 많이 쓰는 분
- 아이가 여행에 흥미를 갖길 바라는 분
- 이동 동선 짜는 게 힘드신 분

---

## 어떻게 사용하나요?

아래 한 줄만 입력하세요:

```
/plan-trip 5월 경주 2박3일 초등5학년 아이와 함께
```

그러면 AI가 알아서 합니다:

1. **후보 여행지 7개+ 탐색** — 역사·교육 가치 높은 곳 우선
2. **비판적 검토** — 이동 거리, 안전성, 아이 적합도 자동 점검
3. **사용자 선택** — 최종 여행지를 함께 결정
4. **최적 경로 + 시간표** — 하루 운전 4시간 이하 원칙
5. **교육 자료** — 각 여행지의 역사·문화 이야기 (아이 눈높이)
6. **저녁 퀴즈** — 하루 여행을 복습하는 가족 퀴즈
7. **최종 계획서** — 바로 출력해서 쓸 수 있는 여행 계획서

---

## 5분 시작 가이드

### 방법 1: Claude.ai (추천 — 계정만 있으면 됨)

1. [claude.ai](https://claude.ai) 접속 → 로그인
2. 왼쪽 메뉴 **"Projects"** 클릭 → **"New project"**
3. **"Set project instructions"** 클릭
4. [`tier1/claude-project-prompt.md`](tier1/claude-project-prompt.md) 파일 내용을 **전체 복사**해서 붙여넣기
5. **"Save"** 클릭
6. 채팅창에 `/plan-trip 여행조건` 입력 → 완료!

### 방법 2: Gemini (무료 한도 가장 넉넉함)

1. [gemini.google.com](https://gemini.google.com) 접속 → 로그인
2. 왼쪽 메뉴 **"Gems"** → **"새 Gem 만들기"**
3. [`tier1/gemini-gems-prompt.md`](tier1/gemini-gems-prompt.md) 내용을 지침에 붙여넣기
4. Gem 저장 후 사용

자세한 설정 방법은 **[설정 가이드](tier1/setup-guide.md)** 를 참고하세요.

---

## 샘플 결과물

실제 완성 계획서 예시를 확인해 보세요.

| 샘플 | 테마 | 특징 |
|------|------|------|
| [경주 2박3일](samples/gyeongju-2nights-3days.md) | 신라 천 년 유네스코 탐방 | 석굴암·불국사·대릉원·첨성대·양동마을, 일별 퀴즈 포함 |

> 다른 지역 샘플을 직접 만들어 기여하고 싶다면 [CONTRIBUTING.md](CONTRIBUTING.md)를 참고하세요.

---

## 폴더 구조

```
opensource/
├── README.md                    ← 지금 읽고 있는 파일
├── CONTRIBUTING.md              ← 기여 가이드
├── tier1/                       ← 일반 부모용 (API 불필요)
│   ├── claude-project-prompt.md ← Claude.ai 시스템 프롬프트
│   ├── gemini-gems-prompt.md    ← Gemini Gems 시스템 프롬프트
│   └── setup-guide.md           ← 플랫폼별 설정 가이드
└── samples/                     ← 완성 계획서 예시
    └── gyeongju-2nights-3days.md ← 경주 2박3일 샘플
```

> **Tier 2 (개발자용)** — API 연동, 실제 좌표 계산, NotebookLM 자동화가 포함된
> 파워유저 버전은 프로젝트 루트의 `.cursor/rules/`, `.agent/workflows/`,
> `.claude/skills/` 폴더를 참고하세요.

---

## 기여 방법

- 다른 지역 여행 계획서 샘플을 PR로 공유해 주세요.
- 여행지 교육 자료, 퀴즈 예시, 사용 후기는 [Issue](https://github.com/beausea/trip-planner/issues)로 남겨주세요.
- 자세한 작성 기준과 PR 절차는 **[CONTRIBUTING.md](CONTRIBUTING.md)** 를 확인하세요.

---

## 라이선스

MIT License — 자유롭게 사용, 수정, 배포하실 수 있습니다.
