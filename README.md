<!-- 헤더 이미지 (capsule-render 사용) -->
![header](https://capsule-render.vercel.app/api?type=waving&color=auto&height=250&section=header&text=welcome&fontSize=70&animation=fadeIn&desc=dmk1999s's%20GitHub%20Profile&descAlignY=60&descAlign=62)

## 👋 Hi there, I’m Dmk1999s!

### 🧑‍💻 About Me
- 🎓 Sangmyung University Computer Science major
- 🔭 Interested in **AI**, **Web development**, and **Open Source**


### 📝 Projects
1. 인공지능과 클라우드를 활용한 서비스·콘텐츠 활용 사례 공모전
   > 대학교 챗봇 개발
   > 개발기간: 2024.03.03-2024.04.19
   > 역할: 팀장, 데이터 확보, 모델 훈련
   >> 데이터
   >> - 데이터 수집
   >> - 상명대학교 홈페이지의 정보를 전부 크롤링함
   >> - 수집한 데이터를 의도별로 분류
   >> - 14373개의 텍스트 데이터셋을 확보하였고 훈련 데이터와 검증 데이터를 7:3으로 분리
   >
   >> 모델 훈련
   >> - 데이터 전처리
   >> - 모델 최적화
   >> - 준비한 데이터를 BERT 모델에 파인튜닝 진행
   >> - 파라미터를 조정하여 손실률을 0.2%, 정확도를 88% 까지 향상
   >
   >>  Back-end
   >> - Language : python3
   >> - Skill : Django, Django-rest-framework, PostgreSQL
   >
   >> Front-end
   >> - Language : python
   >> - Skill : Flask
   >>
   >> [프로젝트 상세 설명 https://github.com/Dawonlee0/CampusBot]
   >> 우수상 수상

2. 뤼튼테크놀로지스 - Gen AI 아이디어 톤
   > ### wrtn connecting — GenAI 커뮤니티 & 숏폼 생성 (뤼튼 아이디어톤 본선 진출, 2024)
   > 대회 기간: 2024.04.23-2024.07.12
   > 역할: 팀장, 자료 수집, 아이디어 제시, 피그마로 피피티 제작
   > LLM 채팅 중심의 기존 뤼튼을 넘어, 생성형 AI로 **Shorts·이미지·음악**까지 자동 생성하고 **관심사 기반 커뮤니티**에서 서로 공유·소통하도록 확장한 서비스 콘셉트
   >> 핵심 제안
   >> - **생성 파이프라인**: Chat → 스크립트 요약 → 샷리스트/TTS → **Shorts 자동 생성**
   >> - **커뮤니티 연결**: Q&A 결과에 맞춰 **추천 커뮤니티** 제시
   >> - **서랍장(Library)**: 커뮤니티별 **Shorts / Image / Music**를 모아 **아카이브·재활용**
   >> - **모바일 온보딩**: 홈(탐색) → Q&A(문제 해결) → 커뮤니티(관계) → 서랍장(축적)의 여정 설계
   >
   >> 비즈니스 모델
   >> - **프리미엄 구독**: 생성 횟수 확장
   >> - **B2B/API 라이선스**: 조직/파트너에 **생성 파이프라인·커뮤니티 모듈** 라이선스 제공
   >>

3. 캡스톤 디자인 — **금융상담 챗봇 서비스** (2025 진행 중)
   > RAG + 규칙기반 분석으로 개인의 위험성향·목표에 맞는 금융 정보/상품을 설명하고 추천하는 **대화형 금융 도우미**
   > 개발 기간: 2025.03.01-2025.09.20
   > 역할: 챗봇 서비스 구축
   >> 문제 정의
   >> - 금융 정보가 흩어져 있어 초심자·시니어 사용자가 **이해/비교/의사결정**에 어려움
   >> - 일반 검색/챗은 **개인 맥락(자산·목표·리스크)** 반영이 부족
   >
   >> **솔루션 개요**
   >> - **백엔드**: Django/DRF + Celery/Redis, Docker/Nginx, GitHub Actions CI/CD  
   >> - **데이터**: AWS RDS(MySQL) — `deposit`, `savings`, `annuity`, `krx_stock_info`, `nasdaq_stock_info` 등 도메인 테이블 정규화
   >> - **검색/RAG**: OpenAI 임베딩(1536차원) → **OpenSearch k-NN** 인덱싱과 키워드 기반 검색을 활용한 하이브리드 검색, 메타데이터 필터링(금리, 기간, 위험도, 수수료 등), Agent tool을 생성하여 조건 스크리닝, 특정 종목 조회, 프로필 요약 생성, 검색 체인 툴을 저장하여 llm이 스스로 어떤 툴을 사용할지 결정하고, 필요하면 여러 툴을 순차로 호출해서 최종 답변을 생성하도록 함
   >> - **LLM**: GPT-3.5 turbo 모델에 금융 데이터를 학습하여 파인튜닝 진행하였고 모든 답변에 학습모델을 통해 답변을 가공하도록 함
   >> - **개인화**: 사용자의 목표·리스크 성향·선호(예: 장기/단기, 고정/변동금리)를 **프로필 요약**으로 반영
   >
   >> **주요 기능**
   >> - **AI 재태크 상담**
   >> - **사용자 투자 성향 분석**
   >> - **커뮤니티 플랫폼**
   >> - **크레딧 시스템**
   >
   >> **배포 및 인프라 아키텍처**
   >> - **CI/CD**: GitHub Actions를 통해 코드 변경 시 Docker Hub에 이미지 자동 빌드 및 푸시
   >> - **배포 환경**: AWS EC2 인스턴스에서 Docker 기반 컨테이너 실행 (Nginx + Django + Redis)
   >> - **Nginx**: 리버스 프록시 및 정적 파일 서빙
   >> - **Redis**: 세션/캐시 관리 및 Celery 작업 큐 처리
   >> - **데이터베이스**: AWS RDS(MySQL) 연동
   >> - **검색**: OpenSearch와 연결하여 k-NN 기반 벡터 검색 및 키워드 검색 제공
   >> - **Lambda**: OpenSearch 후처리 및 특정 이벤트 트리거 처리
   >> [프로젝트 상세 설명 https://github.com/NaughtyComputer]
   
### 📫 Contact
- 📧 Email: loik1235@gmail.com

---
