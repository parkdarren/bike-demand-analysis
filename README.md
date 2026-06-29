# Bike Demand Analysis

자전거 대여 수요 데이터를 활용해 시간, 계절, 날씨 변수에 따른 수요 패턴을 탐색하고 예측 모델링을 수행한 분석 프로젝트입니다.

## Project Overview

이 프로젝트는 자전거 공유 서비스의 대여량을 예측하기 위해 데이터 전처리, 탐색적 데이터 분석, 피처 엔지니어링, 모델 학습 과정을 정리한 포트폴리오용 저장소입니다.

## Repository Structure

```text
bike-demand-analysis/
├─ README.md
├─ requirements.txt
├─ notebooks/
│  ├─ 01_eda.ipynb
│  └─ 02_modeling.ipynb
├─ data/
│  ├─ train_data.csv
│  └─ test_data.csv
└─ outputs/
   └─ figures/
```

## Data

- `train_data.csv`: 모델 학습 및 분석에 사용하는 자전거 대여 수요 데이터
- `test_data.csv`: 예측 대상 데이터

## Analysis Workflow

1. 데이터 불러오기 및 기본 구조 확인
2. 날짜/시간 변수 분해
3. 계절, 월, 시간대, 요일별 대여량 패턴 분석
4. 날씨 및 온도 변수와 대여량 관계 확인
5. 모델링을 위한 피처 엔지니어링
6. 예측 모델 학습 및 결과 비교

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```

노트북은 `notebooks/` 폴더에서 실행하며 데이터 경로는 `../data/`를 기준으로 설정되어 있습니다.

## Notes

이 저장소는 수업 실습 내용을 바탕으로 개인 포트폴리오용으로 정리한 프로젝트입니다.
