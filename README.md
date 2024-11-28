# Fashion MNIST Classification Project

## 📖 프로젝트 소개

이 프로젝트는 TensorFlow를 활용하여 **Fashion MNIST** 데이터셋의 의류 이미지를 분류하는 CNN(Convolutional Neural Network) 모델을 구현하는 것입니다. **Fashion MNIST**는 총 10개의 의류 카테고리로 이루어진 흑백 이미지 데이터셋으로, 각 이미지는 28x28 픽셀 크기입니다. 이 프로젝트는 딥러닝 기반의 이미지 분류 문제를 이해하고 해결하는 과정을 학습하는 데 중점을 둡니다.

---

## 🧠 데이터셋 개요

**Fashion MNIST**는 `tf.keras.datasets` 모듈에서 제공되며, 의류 이미지와 그에 대응하는 라벨로 구성되어 있습니다.

- **훈련 데이터**: 60,000개
- **테스트 데이터**: 10,000개
- **클래스 (10개)**
    - T-shirt/top
    - Trouser
    - Pullover
    - Dress
    - Coat
    - Sandal
    - Shirt
    - Sneaker
    - Bag
    - Ankle boot

---

## 📊 모델 구조

이 프로젝트에서는 CNN을 활용하여 이미지의 특징을 추출하고, 분류를 수행합니다.

- **Conv2D Layer**: 이미지 특징 추출
- **MaxPooling2D Layer**: 특징 맵 크기 축소 및 중요한 정보 추출
- **Flatten Layer**: 다차원 데이터를 1차원으로 변환
- **Dense Layer**: Fully Connected Layer로 분류 작업 수행
- **Output Layer**: 소프트맥스 활성화 함수로 확률값 출력

---

## 🏋️‍♀️ 모델 학습

모델은 아래의 파라미터로 컴파일 및 학습됩니다:

- **손실 함수**: `sparse_categorical_crossentropy`
- **최적화 알고리즘**: `adam`
- **평가지표**: `accuracy`
- **에포크 수**: 4

학습은 `trainX`와 `trainY` 데이터를 이용하며, 입력 이미지는 **정규화**(`/ 255.0`)를 통해 0~1 범위로 스케일링됩니다.

---

## ✨ 주요 학습 내용

- **Conv2D 레이어**를 사용하여 이미지의 공간적 패턴 분석
- **Pooling 기법**으로 계산량 감소 및 과적합 방지
- **Flatten 레이어**를 통해 Dense 레이어와 연결
- Fashion MNIST 분류 문제에 적합한 CNN 아키텍처 설계 및 구현
