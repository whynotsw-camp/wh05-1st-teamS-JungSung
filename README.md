# 보행 취약 계층 보호 및 제설 사각지대 해소를 위한 열선 설치 입지 분석

-------------------

# 📑 5기 팀 "정성" 프로젝트 기획서

## 1. 프로젝트 개요
- 프로젝트 주제: **[보행 취약 계층 보호 및 제설 사각지대 해소를 위한 열선 설치 입지 분석]**
- 목표: **지자체 차원에서의 겨울철 보행 취약 계층 및 안전한 주행 환경 조성에 관한 서비스 개발**
  
### 시각적 자료
![프로젝트 기획서 다이어그램] ![Uploading image.png…](https://github.com/user-attachments/assets/06d3c48f-e8ff-46b4-afd2-2206c57a7099)



## 2. 프로젝트 일정
### [프로젝트 일정]
| 작업 항목                  | 시작 날짜   | 종료 날짜   | 기간(일) |
|---------------------------|------------|------------|---------|
| 프로젝트 주제 정의 및 계획 수립  | 2025-03-12 | 2025-03-17 | 6       |
| 아이디어 도출 및 시나리오 작성   | 2025-03-17 | 2025-03-19 | 3       |
| 데이터 수집 및 데이터 전처리 | 2025-03-19 | 2025-03-25 | 7       |
| 요구사항 도출 및 WBS 작성   | 2025-03-25 | 2025-03-25 | 1       |
| 결빙 판단 알고리즘 검토 및 적용    | 2025-03-21 | 2025-03-24 | 4       |
| 최종 검토 및 발표 준비     | 2025-03-24 | 2025-03-26 | 3       |
| 프로젝트 발표              | 2025-03-26 | 2025-03-26 | 1       |
 
  --------------------------

# 🚧 열선 설치 입지 분석 - 작업 분할 구조 (WBS)

## 1. 단계별 작업 구성
### 1. 기획
1.1. 문제 정의
- 겨울철 낙상 및 결빙 사고 현황 분석
- 보행 취약 계층 보호의 필요성과 문제점 도출
- 제설 사각지대 문제 및 기존 대응 한계 파악
  
1.2. 데이터 요구사항 정의
- 필요한 데이터 (교통량, 기상, GIS, 유동 인구, 기존 열선 설치 구역, )
- 데이터 출처 및 접근 방식 (공공 데이터 포털, API, 지자체에 직접 요청)

### 2. 데이터 수집 및 준비 
2.1. 데이터 수집 및 저장
- 기상청 API 호출, 수동 다운로드
- MySQL과 구글 드라이브를 사용해 데이터 저장소 이용
  
2.2. 데이터 전처리
 - 결측치 및 이상치 대체
- 데이터 형식 통일 (격자형 자료), 데이터 클렌징 작업 수행

### 3. 데이터 분석 및 모델링
3.1. 데이터 탐색 및 시각화  
3.2. 모델 선택 및 학습
- 결빙 판단 알고리즘 
3.3. 성능 평가
-  

### 4. 결과 도출 및 보고
4.1. 결과 요약  
4.2. 보고서 작성  
4.3. 최종 발표

  ------------------------------

# 📝 요구사항 정의서

## 1. 기능 요구사항
- [ ] 데이터 수집 기능: [수집 대상 및 방식]
- [ ] 데이터 전처리 기능: [결측치 처리, 이상치 제거 등]
- [ ] 분석 기능: [사용할 알고리즘 또는 분석 기법]
- [ ] 시각화 기능: [대시보드, 차트, 그래프]

## 2. 비기능 요구사항
- [ ] 시스템 안정성: 데이터 처리 시 오류 발생 최소화
- [ ] 성능: 데이터 처리 및 분석 시간 최소화
- [ ] 확장성: 새로운 데이터 추가 및 확장 가능

----------------------------

# 🗂️ 프로젝트 설계서

## 1. 시스템 아키텍처
- **구성 요소**:
  - 데이터 수집 모듈
  - 데이터 전처리 모듈
  - 데이터 분석 및 시각화 모듈

## 2. 데이터 설계
- **데이터 흐름**: 원천 데이터 → 전처리 → 분석 → 결과
- **주요 데이터 속성**:
  - 속성 이름: [예: user_id, timestamp, value]
  - 데이터 유형: [정량, 정성]

## 3. 기술 스택
- **데이터 수집**: Python, Qgis, API 활용
- **분석**: Pandas, NumPy, Scikit-learn
- **시각화**: Matplotlib, Seaborn, Plotly, Geopython

## 4. 예상 문제 및 해결 방안
- **문제**: 데이터 불균형  
  **해결 방안**: SMOTE 기법 활용
