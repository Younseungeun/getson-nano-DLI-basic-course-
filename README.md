# getson-nano(DLI basic course)

## classification
### what was used
- PyTorch(딥 러닝 프레임워크)<=>ResNet-18(=Residual neural network)
### process
1. 데이터 수집
2. 모델 훈련하기-Adam 사용
3. 테스트(라이브 데모)하기
4. 오류 발생 시 1~3과정 반복
### characteristic
- 몇 개의 입력을 이산 출력 값에 매핑합니다.
- 주어진 분류 집합에 대해 입력을 분류합니다.
- 입력 영상의 레이블을 예측합니다.
### precautions
- 모델 훈련시에 모델이 필수 특징들을 학습할 수 있도록 다양한 배경을 제공해야한다
- 모델이 색 변화를 학습할 수 있도록 조명 설정을 변경합니다.
- 레이블 오류가 최소한으로 적은 데이터를 수집하여 데이터에 아웃라이어 또는 노이즈를 줄일 수 있도록 한다.
- 올바른 범주의 데이터응 데이터를 데이터 세트 그룹에 추가하여 모델을 시험합니다.

## regression
### process

## Transfer Learning
: 이미 1000개 이상의 class가 학습되어 있기 때문에 새로운 데이터 세트에 대해서만 훈련하면 됩니다.
