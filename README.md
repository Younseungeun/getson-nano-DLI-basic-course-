# getson-nano(DLI basic course)
### 준비물: 젯슨 나노, sd카드, 와이파이 동글, HDMI 연결선, 젯슨 나노 연결선, 카메라, 키보드, 마우스
- STEP1. 젯슨 나노 설정(우분투 설치)
*우분투란? PC와 TV, 스마트폰과 태블릿에도 쓰이는 만능 OS
1. 젯슨 나노를 연결 준비한다.(SD카드 삽입,마우스,키보드,와이파이,파워 연결)
2. HDMI선을 통해 젯슨 나노와 컴퓨터를 연결한다.
3. 컴퓨터를 HDMI 화면으로 바꿔준 뒤, 설정한다.
----------------------------------------------------------------------------------------------------------------------------------------------
- STEP2. pip 및 jtop 설치
5. 터미널에 #sudo apt-get upgrade  -- 업그레이드 해
6. 터미널에 #sudo apt-get update -- 업데이트 해
7. 터미널에 #sudo apt install python3-pip -- pip(Python에서 작성된 소프트웨어 패키지의 설치 및 관리를 단순화하는 패키지 관리 시스템)설치해
8. 터미널에 #sudo pip3 list -- 설치 되었는지 확인해

* 'sudo'는 리눅스에서 자주 사용되는 명령어로 **Super User Do의 줄임말**
-------------------------------------------------------------------------------------------------------------------------------------------------
- STEP3. 카메라와 냉각팬 연결
6. 카메라 연결 (CSI와 USB카메라 특징 CSI:빠름,안정적,용량 큼, USB:느림,호환성,용량이 작음)
7. 냉긱팬 연결 
8. 냉각팬 작동...터미널에 #sudo sh -c 'echo 128 > /sys/devices/pwm-fan/target_pwm'
9. 상태 확인.....터미널에 #jtop
-----------------------------------------------------------------------------------------------------------------------------------------
- STEP 4. 주피터랩 연결
11. 젯슨 터미널에 #ssh <name>@192.168.55.1 -- 젯슨 나노에 접속
  =>dli@192.168.55.1's password: 패스워드 입력
  => 젯슨 나노에 연결됨
2. #ls -- 디렉토리 안에 어떤 것이 있는지 살펴봐
3. #mkdir -p ~/nvdli-data -- "nvdli-data"라는 dir(디렉토리)생성 해
4. #echo "sudo docker run --runtime nvidia -it --rm --network host \
    --volume ~/nvdli-data:/nvdli-nano/data \
    --volume /tmp/argus_socket:/tmp/argus_socket \
    --device /dev/video0 \
    nvcr.io/nvidia/dli/dli-nano-ai:v2.0.2-r32.7.1" > -- 도커 다운로드 해
5. #docker_dli_run.sh -- 도커 실행해









## 기본지식

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
-------------------------------------------------------------------------------------------------

