# 📚 free-programming-books 분석 & 활용 노트

> 이 레포지토리가 무엇인지, 어떻게 쓰는지, 어떻게 수익화할 수 있는지 정리한 문서입니다.
> 작성일: 2026-09-08

---

## 🔗 관련 링크 (GitHub 주소)

| 구분 | 주소 |
|---|---|
| **내 fork 저장소** | https://github.com/bmshin94/free-programming-books |
| **원본 저장소 (upstream)** | https://github.com/EbookFoundation/free-programming-books |
| **자료 검색 사이트** ⭐ | https://ebookfoundation.github.io/free-programming-books-search/ |
| **정적 웹사이트** | https://ebookfoundation.github.io/free-programming-books/ |
| **관리 재단** | https://ebookfoundation.org |
| **기여 가이드** | https://github.com/EbookFoundation/free-programming-books/blob/main/docs/CONTRIBUTING.md |
| **초보자 HOWTO** | https://github.com/EbookFoundation/free-programming-books/blob/main/docs/HOWTO.md |
| **Good First Issues** | https://github.com/EbookFoundation/free-programming-books/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22 |

### 클론 명령어

```bash
# 내 fork 받기
git clone https://github.com/bmshin94/free-programming-books.git

# 원본 받기
git clone https://github.com/EbookFoundation/free-programming-books.git
```

---

## 1. 이게 뭐야? (한 줄 요약)

> **"공짜 개발 학습자료 링크를 모아놓은 거대한 즐겨찾기 목록"**

- 실행되는 프로그램이 **하나도 없음**. 전부 마크다운(`.md`) 문서 뭉치
- 그래서 **설치라는 개념이 없음** (`npm install` ❌ / `pip install` ❌)
- GitHub 별(star) 개수 **전 세계 최상위권** 레포
- 비영리 **Free Ebook Foundation**이 관리
- 총 자료 링크 수: **13,029개**
- 전체 용량: **3.9MB** (사진 2장 수준)

**비유:** 도서관의 "책 목록표"와 같음. 책 자체가 아니라 *"인터넷에 무료로 공개된 개발 책·강의가 어디 있는지"* 적어놓은 목록.

---

## 2. 폴더 구조 (실제 확인 결과)

| 폴더 | 내용 | 규모 |
|---|---|---|
| **`books/`** | 무료 전자책 목록 | **48개 언어** 파일 |
| ├ `free-programming-books-langs.md` | 프로그래밍 **언어별** (C, Python, Rust…) | **1,870개** 링크 |
| ├ `free-programming-books-subjects.md` | **주제별** (알고리즘, OS, AI…) | **881개** 링크 |
| └ `free-programming-books-ko.md` | **한국어 책** 🇰🇷 | 121개 |
| **`courses/`** | 무료 온라인 강의 | 41개 언어 (한국어 포함) |
| **`casts/`** | 팟캐스트 / 스크린캐스트 | 21개 언어 |
| **`more/`** | 치트시트, 인터랙티브 튜토리얼, 플레이그라운드, 알고리즘 문제집 | 10개 |
| **`docs/`** | CONTRIBUTING, CODE_OF_CONDUCT, HOWTO (한국어판 포함) | 94개 파일 |
| **`scripts/`** | `rtl_ltr_linter.py` — 아랍어/히브리어 등 RTL 언어 검사기 | |
| **`.github/workflows/`** | 자동화 워크플로 | **7개** |
| `_config.yml`, `_includes/` | **Jekyll** 설정 → md를 웹사이트로 자동 변환 | |

> 일반 사용자는 `books`, `courses`, `casts`, `more` **4개만** 보면 됨. 나머지는 관리용.

### 자동화 워크플로 7개 (배울 점 많음!)

| 파일 | 하는 일 |
|---|---|
| `check-urls.yml` | PR에 추가된 **링크가 죽었는지(404) 자동 체크** |
| `fpb-lint.yml` | `free-programming-books-lint` npm 패키지로 **형식/정렬 검사** |
| `detect-conflicting-prs.yml` | 서로 충돌나는 PR 자동 감지 |
| `comment-pr.yml` | PR에 자동 안내 댓글 |
| `stale.yml` | 오래 방치된 이슈 자동 정리 |
| `issues-pinner.yml` | 중요 이슈 자동 고정 |
| `rtl-ltr-linter.yml` | RTL 언어 마크다운 검사 |

👉 **13,000개 링크를 사람 손 안 대고 관리하는 자동화 설계.** GitHub Actions 학습 교보재로 훌륭함.

---

## 3. 사용법

### 방법 1. 웹에서 그냥 쓰기 (설치 0%, 가장 추천)

- 검색: https://ebookfoundation.github.io/free-programming-books-search/
- 웹사이트: https://ebookfoundation.github.io/free-programming-books/
- GitHub에서 바로 보기: `books/free-programming-books-ko.md` 클릭

### 방법 2. 내 컴퓨터로 받기

```bash
git --version                 # Git만 있으면 됨
git clone https://github.com/bmshin94/free-programming-books.git
cd free-programming-books
```

### 방법 3. 받은 폴더에서 자료 찾기

**A. VS Code (추천)**

```bash
code .
```

| 단축키 | 기능 |
|---|---|
| `Ctrl + Shift + F` | 전체 폴더 검색 (가장 많이 씀) |
| `Ctrl + Shift + V` | 마크다운 미리보기 |

**B. 파일 직접 열고 `Ctrl + F`**

| 찾고 싶은 것 | 파일 |
|---|---|
| 언어별 책 | `books/free-programming-books-langs.md` |
| 주제별 책 | `books/free-programming-books-subjects.md` |
| 한국어 책 🇰🇷 | `books/free-programming-books-ko.md` |
| 한국어 강의 🇰🇷 | `courses/free-courses-ko.md` |
| 치트시트 | `more/free-programming-cheatsheets.md` |
| 코딩 문제집 | `more/problem-sets-competitive-programming.md` |

**C. 터미널 (실제 동작 검증 완료)**

```bash
# 특정 언어 책 찾기
grep -A 200 "^### Python" books/free-programming-books-langs.md | grep -E "^\* \[" | head -10

# 한국어 자료만 찾기
grep -A 30 "^### Python" books/free-programming-books-ko.md | grep -E "^\* \["

# 전체 폴더에서 키워드 검색
grep -rn "React" books/ courses/ | head -20
grep -rni "머신러닝" books/ courses/

# 어떤 카테고리가 있는지 보기
grep "^### " books/free-programming-books-langs.md
```

### 방법 4. 최신 상태로 업데이트

**GitHub 웹에서 (쉬움):** 내 fork 페이지 → `Sync fork` → `Update branch` → 이후 `git pull origin main`

**명령어로:**

```bash
git remote add upstream https://github.com/EbookFoundation/free-programming-books.git  # 최초 1회
git fetch upstream
git merge upstream/main
```

### 방법 5. 오픈소스 기여 (PR 올리기)

**작성 형식 (이거 안 지키면 봇이 바로 빨간불):**

```markdown
* [책 제목](https://링크주소) - 저자이름 (파일형식) (라이선스)
```

**필수 규칙 5가지**

1. 가나다 / ABC 순 **정렬** 지키기
2. `*` 로 시작 (`-`, `+` 금지)
3. **진짜 무료**여야 함 (회원가입·이메일 강제 = 거절)
4. `https://` 우선
5. 한 PR = 한 가지 작업

**PR 올리는 순서**

```bash
git checkout -b add-python-book        # 새 브랜치 (main에서 직접 작업 금지)
# 파일 수정
git diff                                # 확인
git add books/free-programming-books-ko.md
git commit -m "Add 점프 투 파이썬 (Korean)"
git push -u origin add-python-book
```

→ GitHub의 `Compare & pull request` 버튼 → 설명 작성 → `Create pull request`
→ 자동 검사 봇 7개 통과(초록불 ✅) → 관리자 리뷰 → 머지 🎉

---

## 4. 라이선스 (수익화 전 필독)

### ✅ 이 저장소: **CC BY 4.0** (Attribution 4.0 International)

`LICENSE` 파일 확인 결과 **NonCommercial(비상업) 조항이 없음.**

| 가능 | 조건 |
|---|---|
| ✅ 상업적 이용 | 돈 벌어도 됨 |
| ✅ 수정 · 재가공 | 자유 |
| ✅ 재배포 | 자유 |
| ⚠️ **출처 표기 필수** | "EbookFoundation/free-programming-books 기반" 명시 |

### 🚨 절대 하면 안 되는 것

**"링크 목록"은 CC BY지만, "링크가 가리키는 책들"은 각자 다른 저작권임.**

| 금지 | 이유 |
|---|---|
| ❌ 책 PDF를 긁어서 파일로 판매 | 명백한 저작권 침해 |
| ❌ PDF 모아서 "이북 패키지" 배포 | 위와 동일 |
| ❌ 원 저작자 이름 지우고 내 것처럼 | 라이선스 위반 |

👉 **안전선: "링크 · 목록 · 메타정보"까지만 사용. "책 내용"은 절대 손대지 않기.**

---

## 5. 수익화 아이디어

### 핵심 인사이트

> 링크 13,000개 자체는 돈이 안 됨 (이미 전부 공개되어 있음).
> **돈이 되는 건 "가공"이다.** 사람들이 지불하는 건 *자료*가 아니라
> **"내 상황에 맞게 골라주고, 순서를 잡아주는 것"**.

### 발견한 시장 빈틈 🔥

```
영어 자료:  2,659개   ██████████
일본어:       348개   █
중국어:       378개   █
한국어:       114개   ▌        ← 영어의 4%!
```

**한국어 시장이 비어 있음 = 기회.**

### 아이디어 6개 (현실성 순)

| # | 아이디어 | 난이도 | 현실성 | 수익 모델 |
|---|---|---|---|---|
| 🥇 1 | **한국어 학습자료 큐레이션 뉴스레터** | ⭐☆☆☆☆ | ★★★★★ | 스폰서 광고, 제휴 링크, 유료 멤버십 |
| 🥈 2 | **AI 학습 로드맵 생성 SaaS** | ⭐⭐⭐⭐☆ | ★★★★☆ | 월 4,900원 구독 |
| 🥉 3 | **블로그 / 유튜브 콘텐츠** | ⭐⭐☆☆☆ | ★★★★☆ | 애드센스, 제휴마케팅 |
| 4 | 크롬 확장 / VS Code 익스텐션 | ⭐⭐⭐☆☆ | ★★★☆☆ | 프리미엄, 후원 |
| 5 | B2B 신입 온보딩 커리큘럼 납품 | ⭐⭐⭐☆☆ | ★★★☆☆ | 회사당 50~300만원 |
| 6 | 모바일 앱 "공짜 개발서재" | ⭐⭐⭐⭐☆ | ★★☆☆☆ | 광고, 광고제거 |

#### 🥇 1번 — 뉴스레터

- 매주 "무료 자료 5개 + 내 코멘트" 발송
- 이 레포 + 위키독스 + 인프런 무료강의 큐레이션
- 도구: 스티비, 메일리 (무료 시작)
- 구독자 1,000명 → 스폰서 1회 30~100만원 / 인프런·유데미 제휴 링크
- **장점:** 자본 0원, 실패해도 잃을 게 없음, 내 공부도 됨

#### 🥈 2번 — AI 학습 로드맵 SaaS (수익 잠재력 최고)

```
입력: "비전공자인데 3개월 안에 백엔드 취업하고 싶어"
        ↓  [ 13,000개 자료 DB + AI ]
출력: 12주 커리큘럼 + 주차별 자료 + 체크리스트 + 진도율
```

- 기본 무료 / 월 4,900원 프리미엄 (진도 추적, PDF 내보내기, 무제한 생성)
- **"자료 찾기"가 아니라 "순서 정해주기"를 파는 것**

#### 🥉 3번 — 콘텐츠

- 주제: "개발 공부, 돈 한 푼 안 쓰고 하는 법"
- 예: *"파이썬 유료강의 사지 마세요, 이 무료책이 더 좋습니다"*
- "무료 파이썬 책" 류 검색어는 수요가 꾸준함 → SEO 유리

### 추천 전략

```
[1단계] 뉴스레터 (지금 당장, 0원)
   ↓  구독자 = 검증된 고객 + 마케팅 채널
[2단계] AI 로드맵 SaaS (3~6개월 후)
   ↓  뉴스레터 구독자에게 바로 출시 = 초기 유저 확보 완료
[3단계] B2B 확장
```

대부분 실패하는 이유는 *"만들었는데 아무도 안 씀"*. 뉴스레터로 **먼저 사람을 모으면** 제품 출시 시점에 이미 고객이 있음.

### 냉정한 현실 체크

| 항목 | 평가 |
|---|---|
| 💰 단기 수익 | 거의 없음. 3~6개월 무수익 각오 |
| 🏆 경쟁 | roadmap.sh, 인프런 등 강자 존재 |
| ✅ 강점 | **한국어 시장 공백** (114개뿐) |
| ⚠️ 리스크 | 진입장벽 낮음 → **내 관점·신뢰**가 유일한 해자 |
| 🔑 성공 열쇠 | 자료의 "양"이 아니라 **"직접 보고 검증했다"는 신뢰** |

---

## 6. 기술 스택 — React vs PHP

### 데이터 구조 (파싱 대상, 실제 확인 완료)

```markdown
### JavaScript          ← 대분류 (### )
#### React              ← 소분류 (#### )
* [제목](링크) - 저자 (PDF) (CC BY-SA)   ← 실제 자료
```

**파싱 시 주의사항 3가지**

1. 맨 위 `### Index` 섹션은 건너뛰기 → 링크가 `#csharp` 같은 앵커라 실제 자료가 아님
2. `<a id="csharp"></a>C#` ← HTML 태그가 섞여 있음, 제거 필요
3. `####` 소분류가 `langs.md`에만 71개 존재 → 계층 구조로 처리

### 비교표

| 항목 | ⚛️ React (Next.js) | 🐘 PHP (Laravel / WordPress) |
|---|---|---|
| 💰 서버비 | **0원** (Vercel 무료) 🏆 | 월 5,000~10,000원 |
| 🔍 SEO | ★★★★★ (SSG로 13,000페이지 생성) | ★★★★★ |
| 🤖 AI 연동 | ★★★★★ 스트리밍 최강 🏆 | ★★★☆☆ |
| ⚡ 개발 속도 | ★★★★☆ | ★★★★★ (WordPress면 1일컷) 🏆 |
| 💳 결제 연동 | 토스/Stripe 문서 풍부 🏆 | 국내 PG 예제 많음 |
| 🧑‍💻 언어 개수 | JS 하나로 해결 🏆 | PHP + JS 둘 다 |
| 📈 포트폴리오 가치 | ★★★★★ 🏆 | ★★★☆☆ |

### 결론: **React (Next.js) 추천** ⚛️

1. **서버비 0원으로 시작** — Vercel + Supabase 무료 플랜
2. **AI 스트리밍** — 로드맵 생성 10~20초, 화면이 멈추면 이탈. React는 스트리밍이 기본
3. **SSG로 13,000페이지 사전 생성** — 구글 노출 = 애드센스 수익의 핵심

**단, PHP가 나은 경우:**

- 이미 PHP를 훨씬 잘함 (익숙한 게 최고)
- 아이디어 3번(애드센스 블로그)만 빨리 하고 싶음 → **WordPress가 압도적으로 빠름**
- 이미 카페24/가비아 호스팅 보유

### 추천 아키텍처

```
[1단계] 마크다운 파싱 (1회성 스크립트)
   books/*.md  →  data.json (13,029개)
        ↓
[2단계] Next.js 앱
   ├─ /                 메인 (검색)
   ├─ /lang/python      언어별 목록 (SSG = SEO)
   ├─ /ko               한국어 전용 🇰🇷
   └─ /roadmap          ⭐ AI 로드맵 생성기 (수익 지점)
        ↓
[3단계] 백엔드
   ├─ Supabase          회원 / 북마크 / 진도율 (무료)
   ├─ Claude API        AI 커리큘럼 생성
   └─ 토스페이먼츠       구독 결제
```

**기술 스택 (전부 무료로 시작 가능)**

```
Next.js 15 (App Router) + Tailwind CSS + Supabase + Claude API + Vercel
```

---

## 7. 다음 할 일 (TODO)

- [ ] **`parse.js` 작성** — 마크다운 → `data.json` 변환
      (React든 PHP든 **공통으로 필요**. 어떤 스택을 골라도 안 버려지는 핵심 자산 💎)
- [ ] 한국어 자료 114개 품질 분석 → 빈 분야(공백 카테고리) 찾기
- [ ] 뉴스레터 1호 콘텐츠 초안 작성
- [ ] Next.js 프로젝트 셋업 + 검색 화면
- [ ] 오픈소스 첫 PR 올려보기 (`docs/CONTRIBUTING.md` 형식 준수)

### 목표 JSON 스키마

```json
[
  {
    "title": "점프 투 파이썬 - Python 3",
    "url": "https://wikidocs.net/book/1",
    "author": null,
    "category": "Python",
    "subcategory": null,
    "language": "ko",
    "type": "book",
    "formats": []
  }
]
```

---

## 📌 최종 요약

| 목적 | 해야 할 일 |
|---|---|
| 😌 그냥 공짜 책 찾기 | 검색 사이트 즐겨찾기 → 끝 (설치 0) |
| 💻 내 컴에서 보기 | `git clone` → `code .` → `Ctrl+Shift+F` |
| 🔄 최신 유지 | GitHub `Sync fork` → `git pull` |
| 🚀 오픈소스 기여 | `docs/CONTRIBUTING.md` 읽고 → 형식 맞춰 → PR |
| 💰 수익화 | 뉴스레터로 시작 → AI 로드맵 SaaS로 확장 |

---

> 본 문서는 https://github.com/EbookFoundation/free-programming-books (CC BY 4.0) 를 분석한 내용을 담고 있습니다.
