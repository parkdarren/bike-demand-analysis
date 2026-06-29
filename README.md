# Bike Demand Analysis

자전거 대여량을 예측하기 위해 시간·계절·날씨 변수를 다루고 여러 회귀 모델을 비교한 노트북 프로젝트입니다. 시간형 변수를 직접 분해하고 수요 분포를 로그 변환해 보는 등 기본적인 EDA와 모델링 흐름을 연습한 작업입니다.

## 현재 저장소 상태

이 저장소의 노트북은 자전거 수요 데이터의 `datetime`·`season`·`holiday`·`weather`·`temp`·`humidity`·`count` 같은 컬럼을 기준으로 작성되어 있습니다.

다만 현재 `data/` 폴더에 들어 있는 CSV는 노트북이 기대하는 자전거 수요 데이터가 아니라 다른 스키마의 데이터입니다. 따라서 노트북을 그대로 실행하려면 `data/train_data.csv`와 `data/test_data.csv`를 자전거 수요 데이터 형식으로 교체해야 합니다.

포트폴리오에서는 이 프로젝트를 대표작으로 두기보다 EDA와 회귀 모델링 연습 기록으로 보조 배치하는 것이 좋습니다.

## 분석 흐름

- 날짜와 시간을 `year`·`month`·`hour`·`weekday`로 분리
- 대여량 `count`의 분포 확인 및 로그 변환
- 계절·시간대·날씨에 따른 수요 패턴 탐색
- 불필요하거나 누수가 될 수 있는 컬럼 제거
- Linear Regression·Decision Tree·Random Forest 모델 비교
- RMSE 기준으로 모델 결과 확인
- K-Fold와 GridSearchCV를 이용한 간단한 검증 흐름 실습

## 사용 기술

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## 파일 구성

```text
notebooks/
  01_eda.ipynb        데이터 확인과 시각화
  02_modeling.ipynb   전처리와 회귀 모델링
data/
  train_data.csv      실행 전 데이터 스키마 확인 필요
  test_data.csv       실행 전 데이터 스키마 확인 필요
```

## 보완할 점

이 프로젝트는 코드 흐름 자체는 자전거 수요 예측에 맞춰져 있지만 현재 저장소의 데이터 파일과 맞지 않습니다. 포트폴리오에 적극적으로 활용하려면 먼저 데이터 파일을 정리하고 노트북을 처음부터 끝까지 다시 실행한 뒤 결과 그래프와 모델 비교표를 저장하는 것이 좋습니다.
