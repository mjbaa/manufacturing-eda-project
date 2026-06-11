# Manufacturing EDA Project

## 1. 프로젝트 개요

이 프로젝트는 AI 모델 개발을 위한 데이터 분석 기초 역량을 기르기 위해 수행한 제조 데이터 EDA 프로젝트입니다.

AI4I 2020 Predictive Maintenance Dataset을 사용하여 제조 설비의 센서 데이터와 고장 여부 간의 관계를 분석합니다.

## 2. 목표

- Pandas를 활용한 CSV 데이터 처리
- 결측치, 중복값, 이상치 확인
- groupby를 이용한 집계 분석
- Matplotlib을 활용한 데이터 시각화
- 상관관계 분석
- train/test split 수행
- Jupyter Notebook 기반 EDA 리포트 작성

## 3. 사용 기술

- Python
- Pandas
- Numpy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- VS Code
- Git / GitHub

## 4. 프로젝트 구조

```text
manufacturing_eda_project/
│
├── data/
│   └── .gitkeep
│
├── figures/
│   └── 시각화 결과 이미지
│
├── reports/
│   └── 데이터 품질 리포트
│
├── notebooks/
│   └── manufacturing_eda.ipynb
│
├── src/
│   └── .gitkeep
│
├── .gitignore
├── README.md
└── requirements.txt
```

## 5. 데이터셋

사용 데이터셋:

- AI4I 2020 Predictive Maintenance Dataset

원본 데이터는 용량 및 라이선스 관리를 위해 GitHub에 포함하지 않습니다.


## 6. 실행 방법

### 1. 저장소 클론

```bash
git clone <repository-url>
cd manufacturing_eda_project
```

### 2. 가상환경 생성

```bash
python3 -m venv .venv
```

### 3. 가상환경 활성화

```bash
source .venv/bin/activate
```

### 4. 패키지 설치

```bash
pip install -r requirements.txt
```

### 5. Jupyter Notebook 실행

```bash
jupyter notebook
```

또는 VS Code에서 아래 파일을 열어 실행합니다.

```text
notebooks/manufacturing_eda.ipynb
```

## 7. 분석 내용

- 데이터 구조 확인
- 결측치 확인
- 중복값 확인
- 이상치 분석
- 제품 유형별 고장률 분석
- 센서 변수 분포 확인
- 고장 여부별 센서값 비교
- 상관관계 분석
- train/test split

## 8. 결과물

- `notebooks/manufacturing_eda.ipynb`
- `reports/data_quality_report.csv`
- `reports/outlier_report.csv`
- `figures/` 시각화 이미지

## 9. 배운 점

이번 프로젝트를 통해 제조 데이터 분석의 기본 흐름을 학습합니다.

특히 모델 학습 전에 데이터 품질을 확인하고, 결측치, 중복값, 이상치, 라벨 분포, 변수 간 관계를 파악하는 과정이 중요하다는 점을 익히는 것을 목표로 합니다.


## 주요 분석 결과

- 데이터는 총 10,000행과 14개 컬럼으로 구성되어 있다.
- 결측치는 존재하지 않았다.
- 제품 유형별 고장률은 `L` 타입이 약 3.92%로 가장 높게 나타났다.
- IQR 기준 이상치 후보는 `rot_speed`와 `torque`에서 확인되었다.
- 고장 데이터는 정상 데이터에 비해 `torque`, `tool_wear`가 높고 `rot_speed`가 낮은 경향을 보였다.
- `torque`는 `failure`와 가장 높은 양의 상관관계를 보였다.
- train/test split을 수행하여 이후 머신러닝 모델링을 위한 데이터 분리를 완료하였다.