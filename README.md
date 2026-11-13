Hi there, I'm Junbum (박준범) 👋

AI와 협업해 아이디어를 게임·웹 서비스로 끝까지 완성하는 메이커입니다.

💼 Notion Portfolio: 👉 상세 포트폴리오 보러가기
📧 Email: junbum8398@gmail.com
🛠️ Core Tech: Godot 4 (GDScript), Python, FastAPI, Django, PostgreSQL, Groq LLaMA 3.3, Google Gemini, Git
🎮 Featured Project: NODEVERSE (진행 중)

자료구조·알고리즘·SQL을 탐험하며 배우는 3D 교육용 게임

저장소: junbum8398-blip/nodeverse-game
개요: 연결된 3D 섬 월드를 로봇으로 탐험하며 23개 실습 미니게임으로 자료구조·알고리즘·SQL·데이터 탐색 개념을 직접 조작해 익히는 교육용 게임 (Godot 4.7, 2인 팀)
담당 영역:
3D 월드 구현: 섬 지형 생성, 섬 간 연결, 플레이어 이동(바다 추락 방지)·카메라 제어
학습 텔레메트리 파이프라인: 시작·실수·되돌리기·클리어 등 플레이 이벤트를 표준 스키마로 수집해 FastAPI 서버로 비동기 전송 (렌더링·조작을 막지 않는 논블로킹 구조)
무중단 안전 장치: 서버 장애·네트워크 단절 시 오프라인 큐로 전환되어 게임이 멈추지 않는 Safe Mode, 3초 타임아웃, F6 인게임 디버그 패널
관리자 대시보드: 실수 히트맵·스테이지별 소요 시간 분석 화면
웹사이트 & AI 안내 로봇 '코봇': 3개 섬 미니게임 웹 체험판과 LLM 기반 안내 챗봇
AI 협업: 기획·구현·디버깅 전 과정에서 AI와 역할을 나눠 협업하고, 문제 정의·작업 분할·결과 검증은 직접 수행
🏋️ Featured Project 2: NetFit (넷핏)

게이미피케이션 기반 공공 체육시설 & 듀얼 AI 피트니스 플랫폼

팀 저장소: encore-ai-campus/mlo-02-p1-team4
배포 주소: https://netfit-production.onrender.com
핵심 기여 및 엔지니어링 성과:
월 0원 비용의 무중단 듀얼 AI: Groq LLaMA 3.3(0.8s) + Google Gemini(0.1s) 자동 폴백 라우터 및 RAG 지식 주입
4.4만 건 공공데이터 정제 파이프라인: 20.3%(9,039건) 결측치 격리 및 Soft Delete를 통한 외래키(FK) 100% 무손실 보존
공공데이터 한계 극복: 시설명/유형 및 요일/시각 연산 기반 실시간 운영시간 및 월요일 정기휴무 판별 엔진
102개 자동화 단위 테스트 전수 통과: 100% Pass (36.4s)
🏥 Featured Project 3: 외래 EMR 메달리온 데이터 파이프라인 & 프로세스 최적화

1,157만 건 대용량 헬스케어 EMR 정제 및 추가 비용 0원의 의료 자원 순환 재배치 실증

팀 저장소: encore-ai-campus/mlo-02-p2-team3
담당 영역: 환자 마스터(patients) 및 외래 예약(appointments, appointment_events) 데이터 파이프라인 총괄
핵심 기여 및 엔지니어링 성과:
대용량 EMR 데이터 품질(DQ) 전수 검증: 환자 마스터(29.1만) 및 사전 예약·이벤트(269.7만) 등 총 298.8만 건 정제 파이프라인 설계
Zero-Drop 무손실 격리 및 2단계 부모키 연쇄 격리(Cascade Quarantine):
시간 역전 이상치($\text{scheduled} < \text{booked}$) 2만 건 및 결측 예약 정밀 격리
상위 예약 격리 시 하위 감사로그(59.6만 건)를 도미노 연쇄 격리하여 클린 DB 내 외래키(FK) 무결성 100.0% 달성 (고아 데이터 0건)
레거시 단절 규명 및 비즈니스 임팩트:
환자의 76.7%(22.1만 명)가 두 병원을 동시 이용함에도 명단이 분리된 문제를 규명하여 '단일 환자 마스터(Master ID)' 통합 근거 실증
추가 비용 0원의 동일 진료과 1:1 순환 파견을 통해 외래 환자 대기시간 43.2% 단축(19.4분 ➔ 11.0분) 달성에 기여
프로덕션 수준의 재현성 확보: 전체 MySQL 실버/DQ 데이터셋을 100MB 깃허브 제한에 맞춘 분할 CSV 및 원클릭 복구 스크립트(Database/build_db.sql) 패키징
