# 개요

- Time Series Analysis
    - 데이터에 **시간** 정보를 독립변수로 사용하는 특징
    - 시간이 연속적으로 배치
        - 로그분석
            - 고객 이탈 예측
                - 다음달에 탈퇴할 회원수 예측
                
            - ..
        - 주가/금융/환율 등 예측 모형
            - 내일 주가 예측
        - IOT/스마트팩토리 예측 모형


# 통계적 시계열 분석

- 종류
    - 단순시계열
    - 모형
        - ETS, Theta, **ARIMA**, VARIMA, BATS/TBATS, ..

## AR 모형

- 자기 회귀 모형
- AutoRegressive Model
- 출력 변수(다음값)가 자신의 이전값, 확률적인 항(불완전하게 예측 가능하게 하는 항)에 선형적으로 의존하여 구하게 되는 모형
- **이전값에 다음값이 영향을 받는 모형**, 평균으로 돌아갈라랴고 하는 경향이 보임

## MA 모형

- 이동 평균 모형
- Moving Average Model
- 데이터의 평균값 자체가 시간에 따라 변화하는 경향을 가짐
- 주식
    - 이동 평균선, (5ma, 20ma, 60ma, 120ma,..)
        - 주가가 특별한 이유 없이 단기 이동 평균선(15|20ma)을 하방 -> 언젠가는 다시 이평선에 수렴하게 된다 -> 매매 기법

## ARMA 모형

- 자기 회귀 이동 평균 모형
- AutoRegressive Moving Average Model
- 2가지 성분을 그대로 적용한 모델(합침)


## ARIMA 모형

- 자기 회귀 + 누적 + 이동 평균 모형
- AutoRegressive Intergrated Moving Average Model

- 전통시계열을 아래 요소 기반으로 분석
    - 규칙성 패턴
        - 이전 결과가 이후 결과에 영햫을 미치는 자기 상관성
        - 이전에 생긴 불규칙한 사건이 나중에 결과에 편향성을 초래하는 이동 평균 형상
    - 뷸규칙한 패턴
        - 특정 확률요소(평균, 분산(표준편차))에 따른 정규분포에서 추출된 임의의 수치

- ARIMA 모형
    - **과거의 데이터가 가지는 추세(momentum, 관성)까지 반영**
        - 차분
    - 선형관계, 추세관계를 모두 고려한 모델
