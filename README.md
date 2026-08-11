# 안녕하세요 👋

백엔드 개발자로 성장하며

반복적인 작업을 자동화하고,
외부 데이터와 서비스를 연결하여
사용자가 실제로 사용할 수 있는 시스템을 만드는 것을 좋아합니다.

Java & Spring Boot 기반 백엔드 개발과
Python 기반 데이터 자동화 프로젝트를 지속적으로 개발하고 있습니다.

# 🚀 About Me

🌱 사이드 프로젝트를 통한 실전 경험 축적

☕ Java & Spring Boot 백엔드 개발

🗄 MySQL 데이터 모델링 및 성능 최적화

🤖 Python 기반 데이터 수집 및 자동화

🚀 GitHub Actions 활용 CI/CD 및 운영 자동화

## 🛠 Tech Stacks

### Languages
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=FFD43B)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)

### Backend & Database
![SpringBoot](https://img.shields.io/badge/springboot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white) 
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white) 
![PostgreSQL](https://img.shields.io/badge/postgresql-4169E1.svg?style=for-the-badge&logo=postgresql&logoColor=white)

### DevOps & Tools
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

### .NET Ecosystem
![.Net](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white) 
![Windows Forms](https://img.shields.io/badge/Windows%20Forms-5C2D91?style=for-the-badge&logo=windows&logoColor=white)

---

## 📌 Featured Projects

### 💰 MoneyLog

지출을 기록하고, 숫자로 이해하는 개인 가계부 웹앱

**Tech Stack**
`Spring Boot` `Spring Security` `JWT` `MySQL` `PostgreSQL` `JPA` `Gradle`

#### What I Solved

* `JwtAuthenticationFilter`를 직접 구현해 Stateless 인증 구조를 구축하고, 로그인 5회 연속 실패 시 15분간 계정을 잠그는 보호 로직 설계
* 도메인별로 흩어져 있던 요청/응답 DTO를 중첩 정적 클래스(nested static class)로 통합해 파일 구조 정리
* 도메인별 예외(`NotFound`, `AccessDenied`, `Duplicate` 등)를 세분화하고 `GlobalExceptionHandler`로 일관된 에러 응답 포맷 구축
* AI 기반 QA 서브에이전트를 별도로 구성해 구현 로직과 분리된 관점에서 검증을 진행, 회원 탈퇴 실패·토큰 미삭제 등 자체 검증만으로는 놓치기 쉬운 이슈 발견

#### Result

* JPQL 기반 집계 쿼리로 기간별 총 지출과 카테고리별 지출 비중을 통계 대시보드로 제공
* DTO 파일 수를 15개 → 8개로 약 47% 축소해 코드 탐색 및 유지보수 편의성 향상
* 별도 QA 프로세스 도입으로 로그아웃/회원 탈퇴 시 토큰이 삭제되지 않는 보안 이슈를 배포 전에 사전 발견 및 수정
* 로컬(MySQL) / 배포(PostgreSQL) 환경을 분리 운영하며 Swagger UI로 API 명세 자동화

🔗 Demo
https://moneylog-4yk2.onrender.com

🔗 Repository
https://github.com/camellia-ver/MoneyLog

---

### 🌤 ClearSky

실시간 기상·대기 데이터를 통합 제공하는 Reactive Web Service

**Tech Stack**
`Spring Boot` `WebFlux` `Reactor` `MySQL` `Chart.js`

#### What I Solved

* 여러 외부 공공데이터 API를 순차 호출하던 구조를 `Mono.zip()` 기반 비동기 병렬 처리로 전환
* 사용자 요청 지역 중심 캐싱 전략을 적용해 동일 지역에 대한 중복 API 호출 제거
* 공공데이터 코드값을 추상화하고 표준화하는 계층을 별도로 설계해 외부 스펙 변경에 대한 영향 최소화

#### Result

* 순차 호출 대비 응답 대기 시간을 줄이고 API 호출 횟수를 감소시켜 서버 부하 완화
* 캐싱 계층 도입으로 동일 요청에 대한 외부 API 의존도 감소
* 표준화 계층 분리로 외부 API 스펙 변경 시 영향 범위를 해당 계층으로 한정, 유지보수성 향상

🔗 Repository
https://github.com/camellia-ver/ClearSky

---

### 📈 Stock Predictor

주가 분석 및 머신러닝 예측 웹 서비스

**Tech Stack**
`Spring Boot` `Python` `scikit-learn` `MySQL` `Chart.js`

#### What I Solved

* 단일 스레드로 전체 CSV를 순회하던 데이터 적재 방식을 Batch 및 병렬 처리 구조로 전환
* pykrx API 호출 시 발생하는 차단(Block) 문제에 대응하기 위해 요청 간격 제어 및 예외 처리 기반의 수집 파이프라인 구축
* 단일 머신러닝 모델의 예측 편차를 보완하기 위해 Random Forest, XGBoost, LightGBM을 결합한 앙상블 구조 적용

#### Result

* 순차 처리 대비 대용량 CSV 적재 시간을 단축하고 초기 로딩 지연 문제 개선
* 요청 제어 및 예외 처리를 통해 데이터 수집 중단 없이 안정적으로 동작하는 파이프라인 확보
* 여러 모델의 예측 결과를 종합해 단일 모델 대비 예측 안정성 향상

🔗 Repository
https://github.com/camellia-ver/stock-predictor

---
### 📈 Stock News Alert

특정 주식 종목의 가격 변동률이 임계값을 초과할 경우, 관련 최신 뉴스를 자동 수집하고 LLM API로 하나의 인사이트로 요약하여 Discord로 전송하는 알림 자동화 서비스

**Tech Stack**
`Python` `FinanceDataReader` `pykrx` `NewsAPI` `Naver News API` `Gemini API` `Discord Webhook` `tkinter`

#### What I Solved

* 주가 데이터와 뉴스 데이터를 결합해 가격 변동이 임계값(예: ±5%)을 초과할 때만 동작하는 이벤트 기반 알림 구조 설계
* pykrx/FinanceDataReader, NewsAPI, Naver News API 등 여러 외부 API의 응답 형식을 통합 처리하는 수집 로직 구현
* 수집된 다수의 뉴스 기사를 Gemini API에 전달해 종목별 하나의 요약된 인사이트로 정리하는 요약 파이프라인 구축
* config.py의 종목 목록·임계값 등 설정값을 코드 수정 없이 변경할 수 있도록 tkinter 기반 GUI 설정 편집기(gui_config.py) 구현

#### Result

* 가격 급등락 발생 시에만 관련 뉴스를 자동으로 수집·요약·전송하여 평소에는 불필요한 API 호출 없이 동작
* 여러 뉴스 기사를 매번 직접 읽지 않아도 LLM이 정리한 하나의 인사이트로 빠르게 상황 파악 가능
* GUI 설정 편집기 도입으로 종목 추가/삭제, 임계값 조정 등 운영 편의성 향상
* Discord Webhook을 통한 실시간 알림으로 별도 알림 서버 없이 즉시 확인 가능

🔗 Repository
https://github.com/camellia-ver/stock-news-alert


---
### ⚾ Baseball Alert

KBO 경기 정보 및 TV 중계 자동 알림 시스템

**Tech Stack**
`Python` `Selenium` `GitHub Actions` `Kakao Talk API` `Discord Webhook`

#### What I Solved

* GitHub Actions의 매 실행마다 환경이 초기화되는 특성으로 인해 DB 없이 상태를 유지해야 하는 문제를 `pending_games.json` 파일 기반 상태 공유로 해결
* 카카오 OAuth 토큰이 만료되면 알림이 끊기는 문제를 Refresh Token 기반 자동 갱신 로직으로 해결
* JavaScript로 동적 렌더링되는 KBO 경기 정보를 Selenium 기반으로 안정적으로 수집

#### Result

* 별도 DB 없이도 워크플로우 실행 간 상태를 유지하며 중복 알림 없이 동작
* Refresh Token 자동 갱신 및 GitHub Secrets 업데이트를 통해 토큰 만료로 인한 알림 중단 없이 지속 운영
* 경기 일정, 결과, 하이라이트 정보를 사람의 개입 없이 자동으로 수집·전송

🔗 Repository
https://github.com/camellia-ver/baseball-alert

---

### 💰 BudgetManager

WinForms 기반 개인 가계부 애플리케이션

**Tech Stack**
`C#` `.NET 8` `WinForms` `ScottPlot`

#### What I Solved

* UI 코드와 비즈니스 로직이 한 클래스에 혼재되어 있던 구조를 MVC 패턴으로 분리
* 사용자마다 다른 형식의 가계부 데이터를 처리할 수 있도록 CSV / Excel Import·Export 기능 구현
* 텍스트 형태로만 확인 가능했던 소비 내역을 ScottPlot 기반 그래프로 시각화

#### Result

* MVC 패턴 적용으로 기능 추가 및 UI 변경 시 비즈니스 로직에 미치는 영향 최소화
* CSV/Excel Import·Export 지원으로 기존에 다른 형식으로 관리하던 가계부 데이터도 그대로 활용 가능
* 소비 패턴을 그래프로 한눈에 확인할 수 있어 텍스트 목록만 보던 것보다 직관적인 분석 가능

🔗 Repository
https://github.com/camellia-ver/BudgetManager

## 🏆 Key Achievements

✅ Spring Security + JWT 기반 인증/인가 시스템 및 계정 잠금 로직 구현

✅ WebFlux + Reactor 기반 비동기 API 병렬 집계 서비스 구현

✅ GitHub Actions 환경에서 JSON 기반 상태 저장 구조 설계

✅ OAuth Refresh Token 자동 갱신 및 Secret 업데이트 자동화

✅ 대용량 주가 데이터 Batch/병렬 적재 및 처리 구조 설계

✅ 외부 API 기반 실시간 데이터 수집·가공·알림 시스템 구축

✅ AI 서브에이전트 기반 QA 프로세스 도입으로 보안 이슈 사전 발견

---
## 📊 GitHub Stats

<p align="left">
  <img height="180em" src="https://github-readme-stats.shion.dev/api?username=camellia-ver&theme=github_dark_dimmed&hide_border=false&include_all_commits=true&count_private=false&hide_rank=true&hide=stars,prs,issues,contribs"/>
  <img height="180em" src="https://github-readme-stats.shion.dev/api/top-langs/?username=camellia-ver&theme=github_dark_dimmed&hide_border=false&include_all_commits=true&count_private=false&layout=compact"/>
</p>

---

## 🎯 Currently Learning
* Spring Security & JWT
* Docker & Containerization
* Cloud Deployment
* AI 활용 개발 생산성 향상
* 대규모 서비스 아키텍처

## 🎯 Next Challenges

* Spring Security + JWT 인증 시스템 구현
* 프로젝트 서비스 배포 및 운영 경험 쌓기
* Docker 기반 개발 환경 구축
* AI를 활용한 개발 생산성 향상
* 대규모 서비스 아키텍처 학습

---

## 📫 Contact

* 📧 Email: jakahi435@gmail.com
* 💻 GitHub: [@camellia-ver](https://github.com/camellia-ver)
