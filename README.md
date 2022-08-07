pceoCnnDeepLearning-python-kaggle
=================================
# About Project
## Purpose
2022-pceo-tasting-deeplearning kaggle 대회 출전 코드입니다.
## About Code
파이썬의 ```tensorflow```를 사용해 CNN을 비롯한 딥러닝 프로그램을 코딩했습니다. (```pandas```,```numpy```) 
## About kaggle competition
### PCEO MNIST
안녕하세요. PCEO MNIST 대회에 오신 것을 환영합니다. 8월 7일 오늘, 짧은 대회를 안내해드릴 대회 호스트 조교입니다. 본격적인 대회에 앞서서 아래의 내용들을 꼭 읽어보시고 참여해주시면 좋겠습니다.

### 대회 개요
이번 대회는 CNN을 이용한 이미지 분류를 수행합니다. 여러분들이 분류를 하게 되는 사진은 한글 손글씨 이미지입니다.
피씨이오딥러닝전문과정탕험 총 13가지 손글씨를 분류해야 합니다. 약 22000여 장의 사진이 훈련과 validation을 위해 주어지게 되며, 각 사진들은 28*28 해상도를 가지고 있습니다.

### Evaluation
이번 대회에의 평가 방식으로 Categorization Accuracy를 사용합니다. 각 사진을 13개의 클래스 중 하나로 예측을 하고, 그것이 정답인지 아닌지로 점수를 구합니다.
아래 코드를 사용하여 계산할 수 있습니다.
```python
from sklearn.metrics import accuracy_score
accuracy_score(y_pred, y_true)
```
### Files
```./input/pceo-mnist/```
| 이름 | 설명 |
| -- | -- |
| train | 훈련을 위한 이미지들의 모임. 각 폴더가 각 class의 이름입니다. |
| test | 예측해야 할 이미지입니다. |
| sample_submission.csv | submission을 위한 샘플 파일입니다. |

# Competition Submision Result
| index | Private Score | Public Score | 비고 |
| - | ----- | -------| --|
|1| 0.92457 |0.92666 | Data Augmentation 추가 |
|2| 0.95806 |0.96190 | dropout, additional dense layers 추가<br>epochs증가 |
|3| 0.96796 |0.96475 | MaxPool2D 추가 , 기타 값 수정|
|4| 0.92195 |0.91990 | Batch Normalization 추가, epochs 증가 <br> ***OVER FITTING***|
|5| 0.96185 |0.96831 | early stopping 추가<br>optimizer ```Adam```에서```Adagrad```로 변경|
