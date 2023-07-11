# 머신러닝 미니 프로젝트 저장소

ML 기반 알고리즘 기능 및 장단점을 학습하기 위해 수행한 미니 프로젝트 작업 과정을 본 저장소에 기록했습니다.
#### 활용 데이터 출처 -
#### 데싸노트의 실전에서 통하는 머신러닝(2022)

---

## datasets 폴더

미니 프로젝트 수행 시 활용한 데이터 셋을 모아 놓은 폴더입니다.

---

## 보험료 예측_linear_regression
### 2022.02.03 ~ 2022.02.10

* 간단하게 아플 가능성이 더 높아보이는 사람에게 더 높은 보험료가 책정된다고 생각할 수 있지만, 실제로 보험료 계산은 상당이 복잡하고 사람마다 각각 다르게 책정됩니다.

* 독립 및 종속 변수가 선형 관계에 놓여있을 때 적합하고 다른 regression 모델과 성능을 비교하는 baseline으로 사용되는 선형 회귀 알고리즘을 데이터셋에 적용 후,
보험료 예측을 위한 작업을 수행했습니다.

---

## 비지도 학습_PCA
### 2022.03.02 ~ 2022.03.09

* 첫번째 작업은 K-means clustering 작업에서 예측 결과가 포함된 최종 고객 분석 데이터셋을 활용했습니다.

* 두번째 작업은 독립변수가 1000개가 넘고 변수명이 없는 데이터셋을 활용했으며, PCA 전과 후 모델 학습 시간이 얼마나 단축되는지 확인했습니다.

* 수많은 독립 변수의 갯수를 줄이면서 가능한 그 특성을 보존해내고 기존 변수 정보를 반영하는 새로운 변수를 만드는 차원 축소 작업을 PCA를 활용해 수행했습니다.

---

## 비지도 학습_k_means_clustering
### 2022.02.17 ~ 2022.02.24

* 첫 번째 데이터는 변수들에 의미가 없는 단순 학습 목적으로 만들어진 인위적 데이터, 두 번째 데이터는 LightGBM 모델링 작업 시 사용한 고객 데이터 중 일부 변수와 정보를 담은 데이터셋입니다.

* 데이터를 적절한 수의 그룹으로 나누고, 그룹의 특징을 살펴볼 수 있는 K-means clustering 알고리즘을 해당 작업에 활용했습니다.

---

## 생존자 예측_logistic_regression
### 2022.03.16 ~ 2022.03.23

* 타이타닉 사고 당시 승선한 승객의 정보를 담고있는 데이터셋입니다(이름, 성별, 나이, 티켓 번호 등).

* 독립 및 종속 변수가 선형 관계에 놓여있을 때 적합하고 다른 분류 모델과 성능을 비교하는 baseline으로 사용되는 로지스틱 회귀 알고리즘을 데이터셋에 적용했습니다.

* 여러 정보가 실제로 승객의 생존에 어떤 영향을 미치는지 예측하기 위한 작업을 수행했습니다.

---

## 스팸 메일 분류_naive_bayes
### 2022.04.01 ~ 2022.04.08

* 스팸 문자에 대한 데이터로, 독립변수는 text 하나밖에 없는 데이터셋입니다. 문장에 사용된 단어를 사용 빈도로 구분해 스팸 여부를 판단하기 위한 작업을 진행했습니다.

* 독립 변수의 종류가 매우 많고, 자연어 처리에 가장 적합한 나이브 베이즈 알고리즘을 활용해 해당 분석 및 스팸 여부 판단 작업을 수행했습니다.

---

## 연봉 예측_decision_tree
### 2022.06.01 ~ 2022.06.08

* 종속 변수가 class(연봉 50000달러 이상/ 50000달러 이하) 로 이루어진 민간인 데이터셋입니다.

* 학력, 혼인 상태, 직업 등의 독립 변수를 활용해 민간인의 연봉 예측 모델링 작업을 진행했습니다.

* 트리 그래프를 통한 탁월한 시각화, 다양한 트리 모델의 baseline으로써 사용되는 의사결정나무 알고리즘을 연봉 예측 작업에 적용했습니다.

---

## 와인 등급 예측_KNN
### 2022.04.15 ~ 2022.04.22

* 총 세가지 등급으로 이루어진 와인의 정보를 담은 데이터셋입니다(알코올, 말산, 마그네슘 수치 등).

* outlier가 적은 데이터에 적합하고 다중 분류 예측에 간편히 활용될 수 있는 KNN 알고리즘을 데이터셋에 적용 후, 와인 등급 예측 작업을 수행했습니다.

---

## 중고차 가격 예측_random_forest
### 2022.06.15 ~ 2022.06.22

* 종속 변수(target) 는 판매 가격, 독립 변수로는 생산년도와 주행거리, 변속기와 마일리지, 배기량 등이 있습니다.

* 앙상블 기법을 사용한 트리 기반 모델 중 가장 보편적인 랜덤 포레스트를 활용해 중고차 가격 예측 작업을 수행했습니다.

---

## 커플 성사 여부_XGBoost
### 2022.07.02 ~ 2022.07.09

* 스피드 데이팅은 남녀 수십 쌍이 짧은 시간을 보낸 뒤, 서로에 대한 호감도를 표현하여 짝을 매칭하는 이벤트입니다.

* 독립 변수로는 상대방과 내 정보, 개인 취향, 상대방에 대한 평가 등이 있고 target 변수는 매칭 성사 여부 입니다.

* 순차적으로 tree를 만들어 이전 트리로부터 더 나은 트리를 만들어내는 특징을 가지는 XGBoost를 본 작업에 적용했습니다.
