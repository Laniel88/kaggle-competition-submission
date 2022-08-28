Kpop_idol_face_identification-CNN-python
========================================

# About Project

## Competiton

`K-pop Idol Face Identification` Competition 대회(kaggle) 출전 코드입니다.

## Library

```
tensorflow
numpy
pandas
sklearn

matplotlib
PIL

os
cv2
random
```

## About kaggle competition

저희 EDA는 이번 방학동안 K-pop 아이돌 팬이 되어버리고 말았습니다. 제 오른쪽에 앉은 -- 씨는 블랙핑크를, 제 왼편에 앉은 --씨는 김민주 그리고 조유리의 팬이 되었습니다… 그런데 동아리 공용 폴더에 정리도 안하고 아이돌 사진을 무지성으로 저장하고는 어디에 누가 있는지 알지를 못하는 거죠… 참으로 슬프게도 이들 사이에 있는 --씨는 짬이 덜차 그들의 덕질을 막을 수 없습니다. 가운데있는 --씨는 삭제하였다간 양각에 놓여 양 옆구리를 가격당할 것이 뻔하기 때문에, 그들의 사진을 잘 정리하여 다른 하드에 저장해두기로 결정합니다. 지금 그들의 사진 저장 속도를 미루어보아 이틀안에 이 문제를 해결하여야 합니다. 아뿔싸… --씨는 개발 초보라 아이돌 사진 분류기를 이틀안에 완성하기는 어려워보이는군요… 여러분.. 불쌍한 --씨를 도와 EDA를 위기에서 구출해주세요!

### Task : 아이돌 분류 모델 만들기

여러분에게는 512\*512 사이즈의 고화질 k-pop 여자 아이돌이 라벨링된 얼굴 사진들이 주어졌습니다. 이를 이용하여 김 모씨와 권 모씨가 사랑하는 리사, 로제, 지수, 제니, 민주, 조유리를 잘 분류할 수 있는 AI 모델을 부탁드립니다!

### Evaluation

Categorization Accuracy를 사용합니다.

## Files

### BASE

`./input/pceo-mnist/`
| 이름 | 설명 |
| -- | -- |
| `train/` | 훈련을 위한 이미지들의 모임. 각 폴더가 각 class의 이름입니다. |
| `test/` | 예측해야 할 이미지입니다. |
| sample_submission.csv | submission을 위한 샘플 파일입니다. |

### additional files

`./input/k-pop idoldentification align face/`

> [mediapipe](https://github.com/google/mediapipe) 를 통해 얼굴의 눈, 코, 입의 위치가 동일하게 정렬한 사진

```
align_test/
align_train/
```

# Competition Submision Result

| index | Private Score | Public Score | 비고 |
| ----- | ------------- | ------------ | ---- |
| final | 0.94642       | 0.95048      | -    |
