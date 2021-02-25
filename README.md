# **Kaggle-petals-to-the-metal**
![kaggle](https://user-images.githubusercontent.com/46522501/106559208-6b87d400-6568-11eb-8e2c-c182f252609f.PNG)
https://www.kaggle.com/c/tpu-getting-started


##
```
from kaggle_datasets import KaggleDatasets
GCS_DS_PATH = KaggleDatasets().get_gcs_path('tpu-getting-started')
print(GCS_DS_PATH)
```
KaggleDatasets 모듈 문제가 생겼다. 

데이터 불러오기를 다른 방법으로 해보자. **케글 API**를 사용해 데이터를 다운받았다. +unzip
```
!kaggle competitions download -c tpu-getting-started
```

![dataload](https://user-images.githubusercontent.com/46522501/106558378-f8ca2900-6566-11eb-9206-1ad4cdba019a.PNG)

![unzip](https://user-images.githubusercontent.com/46522501/106558489-2dd67b80-6567-11eb-9d5b-47551df69474.PNG)





이후 필요한 함수들을 써주었고 준비한 데이터를 사용하기 위한 함수를 작성해주었다.
![def](https://user-images.githubusercontent.com/46522501/106558610-64ac9180-6567-11eb-8db0-24b78f5c1fb1.PNG)




pretrained_model을 가져오고 모델을 만들어준 후 학습시키기 위해 아래 코드를 실행시켰다.
```
historical = model.fit(training_dataset, 
          steps_per_epoch=STEPS_PER_EPOCH, 
          epochs=EPOCHS, 
          validation_data=validation_dataset)
```

...작성중
