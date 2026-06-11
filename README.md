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
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white) 
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=FFD43B)

### Backend & Database
![SpringBoot](https://img.shields.io/badge/springboot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white) 
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white) 

### DevOps & Tools
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

### .NET Ecosystem
![.Net](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white) 
![Windows Forms](https://img.shields.io/badge/Windows%20Forms-5C2D91?style=for-the-badge&logo=windows&logoColor=white)

---

## 📌 Featured Projects

### 🌤 ClearSky

실시간 기상·대기 데이터를 통합 제공하는 Reactive Web Service

**Tech Stack**
`Spring Boot` `WebFlux` `Reactor` `MySQL` `Chart.js`

#### What I Solved

* Reactor `Mono.zip()` 기반 비동기 병렬 API 처리
* 사용자 요청 지역 중심 캐싱 전략 적용
* 공공데이터 코드값 추상화 및 표준화 계층 설계

#### Result

* API 호출량 및 서버 부하 감소
* 응답 지연 최소화
* 외부 API 의존성 감소 및 유지보수성 향상

🔗 Repository
https://github.com/camellia-ver/ClearSky

---

### 📈 Stock Predictor

주가 분석 및 머신러닝 예측 웹 서비스

**Tech Stack**
`Spring Boot` `Python` `scikit-learn` `MySQL` `Chart.js`

#### What I Solved

* 대용량 CSV 데이터 적재 시 발생하는 초기 로딩 지연 문제 개선
* pykrx API 차단 문제 대응을 위한 안정적인 수집 파이프라인 구축
* 머신러닝 모델 단일 예측의 한계를 보완하기 위한 앙상블 모델 적용

#### Result

* Batch 및 병렬 처리를 통해 데이터 적재 시간 단축
* 예외 처리 및 요청 제어를 통해 데이터 수집 안정성 확보
* Random Forest, XGBoost, LightGBM 기반 예측 결과 제공

🔗 Repository
https://github.com/camellia-ver/stock-predictor

---
### 📈 Stock News Alert

주가 변동률이 임계값을 초과할 경우 관련 뉴스를 자동 수집하여 Discord로 전송하는 자동화 서비스

**Tech Stack**
`Python` `pykrx` `NewsAPI` `Discord Webhook`

#### What I Solved

* 주가 데이터와 뉴스 데이터를 결합한 이벤트 기반 알림 시스템 구현
* 여러 외부 API를 활용한 데이터 수집 및 통합 처리
* 임계값 기반 모니터링을 통한 자동 뉴스 탐지 프로세스 구축

#### Result

* 가격 급등락 발생 시 관련 뉴스를 자동 수집 및 전송
* 사용자 개입 없이 동작하는 모니터링 파이프라인 구축
* Discord 기반 실시간 알림 시스템 구현

🔗 Repository
https://github.com/camellia-ver/stock-news-alert


---
### ⚾ Baseball Alert

KBO 경기 정보 및 TV 중계 자동 알림 시스템

**Tech Stack**
`Python` `Selenium` `GitHub Actions` `Kakao Talk API` `Discord Webhook`

#### What I Solved

* GitHub Actions 환경에서 별도 DB 없이 상태를 유지해야 하는 문제 해결
* 카카오 OAuth 토큰 만료로 인한 인증 실패 문제 자동화
* 동적으로 렌더링되는 KBO 경기 정보의 안정적인 수집 구현

#### Result

* `pending_games.json` 기반 워크플로우 간 상태 공유 구현
* Refresh Token을 활용한 OAuth 토큰 자동 갱신 및 GitHub Secrets 업데이트
* 경기 일정, 결과, 하이라이트 정보를 자동으로 수집·전송하는 알림 시스템 구축

🔗 Repository
https://github.com/camellia-ver/baseball-alert

---

### 💰 BudgetManager

WinForms 기반 개인 가계부 애플리케이션

**Tech Stack**
`C#` `.NET 8` `WinForms` `ScottPlot`

#### What I Solved

* UI와 비즈니스 로직이 혼재되는 데스크톱 애플리케이션 구조 개선
* 다양한 형식의 가계부 데이터를 유연하게 관리할 수 있는 파일 처리 기능 구현
* 사용자의 소비 패턴을 직관적으로 파악할 수 있는 시각화 기능 제공

#### Result

* MVC 패턴을 적용하여 유지보수성과 확장성 확보
* CSV 및 Excel 기반 데이터 Import / Export 기능 구현
* ScottPlot을 활용한 자산 및 소비 통계 시각화 제공

🔗 Repository
https://github.com/camellia-ver/BudgetManager

## 🏆 Key Achievements

✅ WebFlux + Reactor 기반 비동기 API 집계 서비스 구현

✅ GitHub Actions 환경에서 JSON 기반 상태 저장 설계

✅ OAuth Refresh Token 자동 갱신 및 Secret 업데이트 자동화

✅ 대용량 주가 데이터 병렬 적재 및 처리 최적화

✅ 외부 API 기반 실시간 데이터 수집·가공·알림 시스템 구축

---
## 📊 GitHub Stats
![](https://github-readme-stats.shion.dev/api?username=camellia-ver&theme=github_dark_dimmed&hide_border=false&include_all_commits=true&count_private=false&hide_rank=true&hide=stars,prs,issues,contribs)<br/>
![](https://github-readme-stats.shion.dev/api/top-langs/?username=camellia-ver&theme=github_dark_dimmed&hide_border=false&include_all_commits=true&count_private=false&layout=compact)

---

## 🎯 Currently Learning
Spring Security & JWT

Docker & Containerization

Cloud Deployment

AI 활용 개발 생산성 향상

대규모 서비스 아키텍처

## 🎯 Next Challenges

* Spring Security + JWT 인증 시스템 구현
* 프로젝트 서비스 배포 및 운영 경험 쌓기
* Docker 기반 개발 환경 구축
* AI를 활용한 개발 생산성 향상
* 대규모 서비스 아키텍처 학습

---

## 📫 Contact

E-mail: jakahi435@gmail.com
