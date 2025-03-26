# 보이스피싱 발생 추이 예측을 위한 시계열 모형 연구: 계절성과 외생변수 활용
Time series models for predicting the trend of voice phishing: seasonality and exogenous variables approaches

## Abstract
최근 고금리와 고물가로 인해 민생의 불안정성이 가중되고 있는 현 사회에, 보이스피싱으로 인한 피해액 또한 증가하고 있다. 이러한 범죄는 기술 발전으로 인해 그 형태와 수법이 지속적으로 진화하고 있으며, 피해자들에게 심각한 금전적 및 정신적 피해를 야기하고 있다. 본 연구는 보이스피싱 발생건수를 더 정확하게 예측하기 위하여, 시계열 모형을 연구 비교하는 것을 목표로 한다. 보이스피싱 발생건수 데이터를 기반으로 ARIMA, SARIMA 모형과 외생변수로서 피해액, 검거건수, 검거인원의 조합을 고려한 SARIMAX 모형을 비교 분석한다. 표본 외 예측분석을 수행하여 예측값의 예측 성능을 검증한다. 예측구간을 추정하고 이의 경험적 포함확률을 도출함으로써 예측 모형의 우수성을 확인한다. 2024년 12월까지의 보이스피싱 월별 발생 건수를 예측하여, 향후 보이스피싱 대응 및 예방 전략 수립에 기여하고자 한다.

In recent years with high interest rates and inflations, which worsen people’s lives, voice phishing crimes also increase along with damage. Voice phishing that becomes more evolved by technology developments causes serious financial and mental damage to victims. This work aims to study time series models for its accurate prediction. ARIMA, SARIMA and SARIMAX models are compared. As exogenous variables, the amount of damages and the numbers of arrests and criminals are adopted. Forecasting performances are evaluated. Prediction intervals are constructed along with empirical coverages, which justify the superiority of the model. Finally, the numbers of voice phishing up to December 2024 are predicted, through which we expect the establishment of future prevention strategies for voice phishing.


[논문 링크](http://www.kcgsa.org/html/sub0501.html?pageNm=article&journal=1&code=452769&issue=0&Page=1&year=2024&searchType=title&searchValue=%EB%B3%B4%EC%9D%B4%EC%8A%A4%ED%94%BC%EC%8B%B1%20%EB%B0%9C%EC%83%9D%20%EC%B6%94%EC%9D%B4%20%EC%98%88%EC%B8%A1%EC%9D%84%20%EC%9C%84%ED%95%9C%20%EC%8B%9C%EA%B3%84%EC%97%B4%20%EB%AA%A8%ED%98%95%20%EC%97%B0%EA%B5%AC:%20%EA%B3%84%EC%A0%88%EC%84%B1%EA%B3%BC%20%EC%99%B8%EC%83%9D%EB%B3%80%EC%88%98%20%ED%99%9C%EC%9A%A9)


## 📌 연구 목적
보이스피싱 발생건수의 정확한 예측을 위하여 시계열 모형 비교 분석

기존의 ARIMA, SARIMA 모형 외에 피해액, 검거건수, 검거인원 등의 외생변수를 추가한 SARIMAX 모형의 예측 성능을 검증

## 📊 사용 데이터
기간: 2016년 1월 ~ 2023년 10월 (월별 데이터, 총 94개)

출처: 경찰청 (정보공개포털)

변수: 발생건수 (종속변수), 피해액, 검거건수, 검거인원 (외생변수)

## 🧪 분석 방법
시계열 모형
ARIMA(p,d,q)

자기회귀, 차분, 이동평균을 결합한 전통적 시계열 모형

SARIMA(p,d,q)(P,D,Q,s)

계절성 반영 시계열 모형

SARIMAX(p,d,q)(P,D,Q,s)

외생변수 포함 계절 시계열 모형

## 분석 과정 요약
정상성 검정: ADF Test를 통해 1차 일반 차분(d=1), 계절 차분(D=1) 수행

모델 적합성 비교: AIC, BIC, RMSE, MAE, MAPE, Ljung-Box 잔차 검정 사용

최종 선정 모형: SARIMAX(2,1,1)(0,1,1,4)

외생변수: 피해액, 검거건수, 검거인원

## 📈 주요 결과
모델	AIC	RMSE	MAE	MAPE	적합성
ARIMA	1389.3	429.1	337.4	16.2%	낮음
SARIMA	1327.6	416.2	332.7	16.8%	보통
SARIMAX	1214.3	226.2	179.7	9.5%	가장 우수
예측기간: 2024년 12월까지의 보이스피싱 발생건수 예측

예측 신뢰구간(80%, 95%) 및 경험적 포함확률 분석 결과 → 신뢰성 높음
![image](https://github.com/user-attachments/assets/6f906c59-ddb6-426c-8aea-8499bb39d2d5)


## ✅ 결론 및 기여
SARIMAX 모형이 계절성과 외생변수를 함께 고려함으로써 예측 성능을 크게 향상시킴

기존 연구 대비 예측오차(RMSE, MAE, MAPE) 모두 현저히 개선됨

정책 수립, 수사 자원 배분, 예방 교육 강화 등 실질적 대응 전략 수립에 활용 가능

## 예측 결과

| 연도 | 월  | 예측 하한값 | 예측 발생건수 | 예측 상한값 | 실제 발생건수 |
|------|-----|--------------|----------------|--------------|----------------|
| 2023 | 11  | 938          | 1391           | 1845         | 1761           |
| 2023 | 12  | 1153         | 1653           | 2154         | 1813           |
| 2024 | 1   | 1204         | 1769           | 2334         | 1843           |
| 2024 | 2   | 952          | 1565           | 2179         | 1195           |
| 2024 | 3   | 592          | 1312           | 2033         | 1977           |
| 2024 | 4   | 1044         | 1826           | 2608         | 1780           |
| 2024 | 5   | 874          | 1720           | 2565         | 1639           |
| 2024 | 6   | 752          | 1653           | 2554         | 1618           |
| 2024 | 7   | 1005         | 2012           | 3019         | 1682           |
| 2024 | 8   | 708          | 1783           | 2858         | 1709           |
| 2024 | 9   | 590          | 1734           | 2878         | 1203           |
| 2024 | 10  | 520          | 1727           | 2934         | -              |
| 2024 | 11  | 577          | 1891           | 3206         | -              |
| 2024 | 12  | 47           | 1436           | 2825         | -              |


