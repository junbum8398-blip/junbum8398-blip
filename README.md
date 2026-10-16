# Hi there, I'm Junbum (박준범) 👋
**데이터 파이프라인부터 AI 연동, 웹·앱 서비스 구현까지 End-to-End로 완성하는 엔지니어입니다.**

- 💼 **Notion Portfolio**: [👉 상세 포트폴리오 보러가기](https://grizzled-hen-794.notion.site/3eb6ee5b72b3804c9d5ce55d0e2a8ab8?source=copy_link)
- 📧 **Email**: junbum8398@gmail.com
- 🛠️ **Core Tech**: Python, Django, PostgreSQL, Groq LLaMA 3.3, Google Gemini, Open-Meteo, Git

---

### 🏋️ Featured Project: NetFit (넷핏)
> **게이미피케이션 기반 공공 체육시설 & 듀얼 AI 피트니스 플랫폼**
- **팀 저장소**: [encore-ai-campus/mlo-02-p1-team4](https://github.com/encore-ai-campus/mlo-02-p1-team4)
- **배포 주소**: [https://netfit-production.onrender.com](https://netfit-production.onrender.com)
- **핵심 기여 및 엔지니어링 성과**:
  - **월 0원 비용의 무중단 듀얼 AI**: Groq LLaMA 3.3(0.8s) + Google Gemini(0.1s) 자동 폴백 라우터 및 RAG 지식 주입
  - **4.4만 건 공공데이터 정제 파이프라인**: 20.3%(9,039건) 결측치 격리 및 Soft Delete를 통한 외래키(FK) 100% 무손실 보존
  - **공공데이터 한계 극복**: 시설명/유형 및 요일/시각 연산 기반 실시간 운영시간 및 월요일 정기휴무 판별 엔진
  - **102개 자동화 단위 테스트 전수 통과**: 100% Pass (36.4s)

### 🏥 Featured Project 2: 외래 EMR 메달리온 데이터 파이프라인 & 프로세스 최적화
> **1,157만 건 대용량 헬스케어 EMR 정제 및 추가 비용 0원의 의료 자원 순환 재배치 실증**
- **팀 저장소**: [encore-ai-campus/mlo-02-p2-team3](https://github.com/encore-ai-campus/mlo-02-p2-team3)
- **담당 영역**: 환자 마스터(`patients`) 및 외래 예약(`appointments`, `appointment_events`) 데이터 파이프라인 총괄
- **핵심 기여 및 엔지니어링 성과**:
  - **대용량 EMR 데이터 품질(DQ) 전수 검증**: 환자 마스터(29.1만) 및 사전 예약·이벤트(269.7만) 등 총 298.8만 건 정제 파이프라인 설계
  - **Zero-Drop 무손실 격리 및 2단계 부모키 연쇄 격리(Cascade Quarantine)**: 
    - 시간 역전 이상치($\text{scheduled} < \text{booked}$) 2만 건 및 결측 예약 정밀 격리
    - 상위 예약 격리 시 하위 감사로그(59.6만 건)를 도미노 연쇄 격리하여 클린 DB 내 외래키(FK) 무결성 100.0% 달성 (고아 데이터 0건)
  - **레거시 단절 규명 및 비즈니스 임팩트**:
    - 환자의 76.7%(22.1만 명)가 두 병원을 동시 이용함에도 명단이 분리된 문제를 규명하여 '단일 환자 마스터(Master ID)' 통합 근거 실증
    - 추가 비용 0원의 동일 진료과 1:1 순환 파견을 통해 외래 환자 대기시간 43.2% 단축(19.4분 ➔ 11.0분) 달성에 기여
  - **프로덕션 수준의 재현성 확보**: 전체 MySQL 실버/DQ 데이터셋을 100MB 깃허브 제한에 맞춘 분할 CSV 및 원클릭 복구 스크립트(`Database/build_db.sql`) 패키징
