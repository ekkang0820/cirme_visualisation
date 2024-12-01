# 범죄 발생 시간대 및 지역 분석 프로젝트

## 프로젝트 개요
이 프로젝트는 지역별 및 시간대별 범죄 유형의 차이점을 분석하고 시각화를 통해 특정 지역의 범죄 취약성을 파악하는 것을 목표로 합니다. 이를 통해 각 지역에서 보완할 점을 도출하고 범죄 예방 및 관리에 도움을 주고자 합니다.

## 주요 기능
1. **범죄 데이터 로드 및 전처리**
   - 시간대 및 지역별로 범죄 발생 건수를 집계합니다.
   - 데이터를 `pandas`를 사용하여 병합 및 정리합니다.

2. **데이터 시각화**
   - **시간대별 범죄 분석**
     - Heatmap을 통해 범죄대분류별 시간대별 발생 건수를 시각화합니다.
     - 스택형 바 차트를 통해 시간대별 범죄대분류 발생 건수 분포를 파악합니다.
   - **지역별 범죄 분석**
     - 지역별 범죄 발생 건수를 막대 그래프로 시각화합니다.
     - 상위 10개 도시의 범죄 발생 건수를 강조하여 분석합니다.
   - **인구 대비 범죄 비율**
     - 인구 데이터를 사용하여 각 도시의 인구 대비 범죄 발생 비율을 계산하고, 이를 막대 그래프로 시각화합니다.

3. **데이터 통합**
   - 범죄 발생 데이터와 인구 데이터를 매핑하여, 도시별 인구 대비 범죄 비율을 산출합니다.
   
## 데이터 구조
### 시간대별 범죄 데이터
- `범죄대분류`, `범죄중분류`: 범죄 유형 정보
- `0시00분-02시59분` ~ `21시00분-23시59분`: 시간대별 범죄 발생 건수
- `미상`, `일` ~ `토`: 요일별 범죄 발생 건수

### 지역별 범죄 데이터
- `범죄대분류`, `범죄중분류`: 범죄 유형 정보
- 도시별 열: 각 도시에서 발생한 범죄 건수

### 인구 데이터
- `도시명`: 도시 이름
- `인구수`: 도시별 인구수

## 실행 방법
1. 필요한 라이브러리 설치:
   ```bash
   pip install pandas matplotlib seaborn
   ```
2. 데이터를 `/content` 디렉토리에 저장:
   - `경찰청_범죄 발생 시간대 및 요일_20191231.csv`
   - `경찰청_범죄 발생 지역별 통계_20221231.csv`
   - `인구수.csv`
3. Python 스크립트를 실행하여 결과 확인.

## 결과 예시
### 1. 시간대별 범죄 Heatmap
범죄대분류별로 시간대별 범죄 발생 패턴을 직관적으로 파악할 수 있습니다.

### 2. 지역별 범죄 발생 건수
각 지역에서 발생한 범죄 건수를 비교하여 범죄가 가장 많이 발생하는 지역을 파악합니다.

### 3. 도시별 인구 대비 범죄 비율
인구수에 비례한 범죄 발생 비율을 비교하여 특정 도시의 범죄율이 높은지 파악할 수 있습니다.

## 프로젝트 목표
- 데이터 기반으로 지역 및 시간대별 범죄 취약성을 시각적으로 이해합니다.
- 분석 결과를 통해 범죄 예방 대책을 수립하고, 해당 정보를 지역 사회와 공유할 수 있도록 지원합니다.
