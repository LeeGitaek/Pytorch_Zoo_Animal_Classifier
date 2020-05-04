# Pytorch_Zoo_Animal_Classifier 
Pytorch, Python 을 사용한 동물 7가지 분류  / Binary Classification<br>

Kaggle - Me : https://www.kaggle.com/coolfamily77

## 모델 학습 <br>
**[1] H(x) = softmax 함수로 가설을 설정하였습니다.**  <br>
 > Pandas Library 를 사용하여 csv 파일을 읽음<br>
  <br>F.softmax(x_train.matmul(w)+b, dim=1) <br>
  We know y is 0 or 1 <br>
  H(x)+b => 0 <= H(x) <= 1 ( How : softmax function or sigmoid function ) <br>
  softmax 함수는 0~1 사이의 값 , 전체 합이 1 (정규화)

**[2] 비용 함수 ( Cost Function ) 또는 Loss Function** <br>
 > C(H(x),y) = -ylog(H(x))-(1-y)log(1-H(x)) <br>
   C(H(x),y) = -log(H(x))   : y=1 <br>
   C(H(x),y) = -log(1-H(x)) : y=0 <br>
 
**[3] cost 비용을 최소화 하기 위한 최적화 알고리즘 / 경사하강법** <br>
 > learning _ rate = 0.05 로 설정하였으며,<br>
   epoch = 200001 만큼 학습하였습니다.<br>
   경사하강법 => Cost Function 을 최소화, 많은 최소화 또는 최적화 문제에 사용되며, <br>
              Cost(w,b) 가 주어졌을때 Cost 를 최소화 하기위한 w,b 값을 찾아냄 <br>
              경사하강 기울기는 미분을 사용한다. <br> 
   result : epoch 200000/200000 , cost : 1.166837 <br>
   
**[4] 데이터 예측**<br>
 > 7개의 클래스로 나누어 예측하였음 / 기존의 데이터 예측 정확도는 100.00 %  <br>
   Kaggle score 는 0.80 을 달성하였음. <br>
   id , category 로 csv 파일을 만들어 테스트 데이터를 예측하였음 . <br>
  array([[ 0,  1],
       [ 1,  3],
       [ 2,  1],
       [ 3,  0],
       [ 4,  6],
       [ 5,  3],
       [ 6,  1],
       [ 7,  5],
       [ 8,  4],
       [ 9,  1],
       [10,  4],
       [11,  3],
       [12,  0],
       [13,  0],
       [14,  1],
       [15,  0],
       [16,  5],
       [17,  0],
       [18,  1],
       [19,  1]])
    
