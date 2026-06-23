안녕하세요, 문준상입니다 👋
> \\\*\\\*PLC SW Engineer @ Dahan FA\\\*\\\* · \\\*\\\*M.S. Candidate in Smart Factory Convergence, Sungkyunkwan University\\\*\\\*  
> 산업 현장 경험을 바탕으로 \\\*\\\*FA 설비 제어 + AI 이상 진단\\\*\\\*을 연구합니다.
---
🔧 What I Do
FA 설비 PLC 프로그래밍 — LS Electric(XG5000), Mitsubishi(GX Works2) 기반 설비 설계·커미셔닝
서보 시스템 구성 — Mitsubishi QD77MS4 / MR-J4, LS Electric XGF-PD4H / L7SA
HMI 개발 — GT Designer3 (GOT1000), 데이터 로깅 및 레시피 관리
산업용 통신 — CC-Link IEF Basic, Modbus TCP/RTU, MQTT, FEnet 고속링크
IIoT 데이터 수집 — Python + MX Component로 PLC 레지스터 100ms 샘플링
---
🔬 Research — RT-FAD Framework
> \\\*\\\*RT-FAD: Real-Time Fault and Anomaly Detection for PLC-Controlled Pneumatic Systems Using Response Time Features\\\*\\\*  
> \\\*Junsang Mun, Jongpil Jeong — Submitted to \\\*\\\*MDPI Sensors\\\*\\\*, 2026\\\*
Mitsubishi Q02HCPU PLC 기반 4스테이션 로터리 인덱스 테이블에서 응답 시간(Δt) 단일 피처만으로 3가지 공압 고장 유형 및 재하 손실 시나리오를 실시간 진단하는 프레임워크.
```
PLC Internal Register (D2000\\\~D2014, 15 axes, 100ms)
    └─ Z-score Detector        → Spike-type  (Air Hose Disconnection, Compressor OFF)
    └─ LSTM Autoencoder        → Drift-type  (Air Hose Wear)
         └─ OR Fusion
              └─ Rule-Based Classifier → Compressor Fault / Air Hose Wear / Disconnection
```
Metric	Value
Macro Recall	0.995
F1 — Compressor OFF	0.815 (measured data)
F1 — Air Hose Wear	0.925 (synthetic data)
Macro F1	0.643
> 🔑 추가 센서 없이 PLC 내장 데이터만으로 다중 고장 유형 실시간 분류 최초 시도
---
🏆 Capstone Design Project
PLC 제어 공압 설비의 응답 시간 기반 고장 진단 프레임워크 RT-FAD  
스마트팩토리 캡스톤디자인 1 · 7조 · 성균관대학교 · 2026.03 ~ 2026.06
구분	담당자	역할
팀장	문준상	PLC 프로그램 개발(Δt 연산 로직), MX Component 데이터 수집 파이프라인
팀원	안광현 · 서수민	공압장치 이상탐지 SW 개발
팀원	민경원 · 서현교	재하 데이터 기반 이상탐지 SW 개발
주요 개발 내용
GX Works2 기반 Δt 연산 로직 구현 (D2000~D2014, 15축)
Python 3.11 + MX Component Ver.4 연동 → CSV 수집 (100ms 주기)
정상 165샘플 + 공압기 OFF 295샘플 실측 데이터 수집
에어 호스 노후(드리프트) / 빠짐(스파이크) 시나리오 Synthetic 3,000샘플 생성
재하 신호(D100~D400) × 존재 센서(X207~X20A) 교차 검증 6규칙 탐지, 단위 테스트 22건 통과
---
📄 Publications & Paper Reviews
📌 개인 논문 리뷰 / 구현
#	제목	비고
1	A Deep Learning Model for Remaining Useful Life Prediction of Aircraft Turbofan Engine on C-MAPSS Dataset	C-MAPSS 데이터셋 기반 항공기 터보팬 엔진 RUL 예측 딥러닝 모델 분석
2	Anomaly Transformer: Time Series Anomaly Detection with Association Discrepancy	Association Discrepancy 기반 시계열 이상 탐지 — 오픈소스 구현 및 검토 (repo)
👥 팀 발표 논문
#	제목	저자	저널
1	Industrial Robot Control System with a Predictive Maintenance Module Using IIoT Technology	Wojtulewicz, A.; Chaber, P.	MDPI Sensors 2025, 25, 1154
---
📂 Projects
Repository	Description	Stack
pneumatic_RUL	RT-FAD 프레임워크 구현 — 공압 이상 탐지 + 잔여 수명 예측	Python, LSTM, TensorFlow
Anomaly-Transformer-Analysis	오픈소스 논문 분석 — Anomaly Transformer 구현 및 검토	Python
---
🛠 Tech Stack
PLC / FA
![LS Electric](https://img.shields.io/badge/LS_Electric-XG5000-003087?style=flat-square)
![Mitsubishi](https://img.shields.io/badge/Mitsubishi-GX_Works2-E60012?style=flat-square)
![Modbus](https://img.shields.io/badge/Protocol-Modbus_TCP%2FRTU-555?style=flat-square)
![MQTT](https://img.shields.io/badge/Protocol-MQTT-660066?style=flat-square)
Language / AI
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
---
📊 GitHub Stats
![Joon-tank's GitHub stats](https://github-readme-stats.vercel.app/api?username=Joon-tank&show_icons=true&theme=tokyonight&hide_border=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Joon-tank&layout=compact&theme=tokyonight&hide_border=true)
---
🏢 Experience
기간	소속	역할
2023 ~ 현재	다한FA	PLC SW 개발 엔지니어
2020 ~ 2022	빙그레 남양주 공장	전기 설비 관리
2020	서울과학기술대학교	학부 졸업
---
📫 Contact
![GitHub](https://github.com/Joon-tank)
---
<p align="center">
  <i>"현장에서 나온 문제를 데이터로 풀고, 연구로 검증합니다."</i>
</p>
