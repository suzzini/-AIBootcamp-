#### 손실함수
- 손실 함수는 실제값과 예측값의 차이(loss, cost)를 수치화해주는 함수이다.
- 오차가 클수록 손실 함수의 값이 크고, 오차가 작을수록 손실 함수의 값이 작아진다.
- 손실 함수의 값을 최소화 하는 W, b를 찾아가는것이 학습 목표이다.


1. 회귀문제 : mean_squared_error(평균제곱오차)
    - 연속형 변수를 예측할 때 사용
  
2. 다중클래스분류 : categorical_crossentropy (범주형 교차 엔트로피)
    - 출력층의 활성화 함수명 : 소프트맥스
    - dens의 unit이 2 이상

3. 다중클래스분류 : sparse_categorical_crossentropy
    - 출력층의 활성화 함수명 : 소프트맥스
    - 범주형 교차 엔트로피와 동일하지만 이 경우 원-핫 인코딩이 된 상태일 필요없이 정수 인코딩 된 상태에서 수행 가능.

4. 이진분류 : binary_crossentropy(이항 교차 엔트로피)
    - 출력층의 활성화 함수명 : 시그모이드
    - 해당 손실함수 사용 시, dense 1이여야됨
  
 * * *
#### 이진분류의 경우, 

1) dense(1, activation='sigmoid'), loss='binary_crossentropy'

2) dense(2, activation='softmax'), loss='sparse_categorical_crossentropy' or 'categorical_crossentropy'
