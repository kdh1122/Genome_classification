# DNA_data
## “데이콘 유전체 정보 품종 분류 AI 경진대회”
- 데이콘 유전체 정보 품종 분류 AI 경진대회
- 기간: ‘22년 12월 ~ ‘23년 01월(1개월)
- 성과: 상위 25%
- Tools: Python
<br>


### 👤역할
데이터 분석, 모델 개발
<br>

### 🧐 Main Issues
모델 개발과 파라미터 설정을 통해 98% 이상의 accuracy를 달성하기가 어려웠음. 모델 파라미터 설정이 아닌 데이터 분석을 통한 인사이트 도출이 필요하였음.
다뤄보지 못한 딥러닝 모델이나 XGBoost 등 부스팅 모델을 사용하면 효과가 향상될 것으로 기대됨.

### 🛠️ Resolved
데이터 class의 불균형을 발견해 smote 기법을 활용해 데이터 불균형을 해결해 모델의 정확도를 높이고자 하였음. <br/>
  하지만 데이터 기존의 불균형 샘플들을 보간하여도 모델의 정확도가 향상되지 않음. <br/>
snp_info 데이터를 활용, 데이터를 유전체 그룹 별로 묶어서 학습시켜야 한다는 인사이트를 도출. <br/>
  그룹별로 묶어서 성능을 확인해보고 최종적으로 선택하였음. <br/>
xgboost, catboost, knn모델이 기존에 정확도가 높은 모델이였어서 3가지 모델에 대해 gridsearch를 수행,베스트 parameter와 best snp group을 활용해 모델 학습 후 예측
그중 knn모델이 accuracy 99프로로 향상됨을 확인.

<br>

### 🎯 Result
초기 97%의 정확도를 가진 모델은 로지스틱 회귀 모델이였음.
공모전이 종료된 이후 에도 딥러닝 모델을 공부해가며 모델을 계속 만들어보고 새로운 기법들을 적용해가며 모델을 향상시켜보고자 했음.
최종적으로 그리드 서치, snp grouping을 활용해 유의미한 feature를 선정해 학습시켜 모델의 향상을 확인하였음.
<br>
### ⭐ Learnd Lessons
개발자로서 기존의 기존의 모델보다 향상된 모델을 만들어보고자 하는 마음에 딥러닝 모델들을 공부해가며 꾸준하게 모델을 만들어보고 학습시켜보곤 했음.<br/>
새로운 기법들을 활용해가며 가상의 데이터를 생성해 불균형을 해결하고자 하였음.  <br/>
최종적으로는 불균형을 해결해도 모델이 향상되지는 않았지만 smote기법을 배우게됨.
**공모전이 종료된 이후에도 활용해 볼만한 모델이나 기법을 알게 되면 적용해보고 했던 경험이 데이터 분석가로서 더 나아가게 하는 큰 계기가 되었음.**<br/>
최종적으로는 단순 모델링 과 파라미터 튜닝이 중요한 것이 아닌 **데이터셋에서 인사이트를 도출하고 활용하는것이 데이터 분석가로서 중요한 역량**이라는 것을 알게됨.
**많은 노력과 경험이 담긴 공모전이였습니다.**

