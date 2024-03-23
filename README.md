# america_sign_language_classifier


### 사용 데이터셋

---

kaggle - https://www.kaggle.com/datasets/datamunge/sign-language-mnist


kaggle에서 제공되는 미국 수화 데이터셋을 이용, 간단한 A~Z 까지의 수화 표현 데이터셋이 존재한다.


### Introductoin

---

CNN 알고리즘을 이용한 간단한 Image Classifier을 구현하였다.

![model](https://github.com/seyeonJeong/america_sign_language_classifier/blob/main/model.PNG)

conv layer -> conv layer -> pooling -> conv layer -> pooling -> FC -> FC (softmax) 의 구조로 구현하였다. 

Dropout : 과적합 방지를 위해 사용, 랜덤으로 해당 노드를 비활성화한다.

Flatten : FC층으로 입력하기 위해 1차원의 벡터로 만들어 준다. (conv layer에서는 width*height*1(or 3(color))의 차원을 사용한다.)

![accuracy](https://github.com/seyeonJeong/america_sign_language_classifier/blob/main/accuracy_loss_graph.PNG)


Test 데이터에 대한 정확도는 약 94%가 나왔고 validation loss와 loss값의 그래프를 출력.



### Result

---

위에서 측정 했듯이 Test 데이터에 대한 정확도는 약 94%가 나왔고, 100개 테스트 데이터에서의 오류값은 8개가 나왔다.

![result](https://github.com/seyeonJeong/america_sign_language_classifier/blob/main/result.PNG)



### Conclusion

---

현재 이미지 처리에서 강력한 성능을 보이는 CNN에 대하여 학습한 후 간단한 구현을 해보았다. 

컨볼루션 layer 이외에도 Dropout, Flatten 등 keras에서 제공하는 다양한 layer를 사용하여 모델을 구현하였다. 

다양한 분야에서 CNN을 통한 Classifier를 만들 수 있다는 생각이 들었으며, 추후 내가 찍은 수화 사진에 대해서도 분류가 가능할지 적용해볼 계획이다.
