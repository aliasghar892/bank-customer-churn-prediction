# bank customer churn prediction

based on dataset from Kaggle
given customers data , the task is to predict customer churn.
it's a binary classification problem
**data is imbalanced**

final result :
random forest model choosed for this task ( it has a good auc score )<br>
in this task reducing false negatives is much more important <br>
predicting false not churn will have **very high impact** (some one hase been churned and we did not found out !)<br>
predicting false churn has lower impact. ( someone has not churned but we falsly predicted he that he does , it does not have very high business impact , just some adittional researches about customer will be done )<br>
so reducing false negatives is important for us , it means that **recall** is more important for us<br>
i reduced false negatives from 480 to 147 but false positive has been increased<br>
this caused the racall 20% improvment, recall is 71% now<br>
before tuning recall was around 75% but model was overfitting<br>
f1 score is around 60%<br>
test score is around 81%

**because of the randomness of random forest, result will be different (but close) in each run**

# update

with t-sne showed that standard scaler will increase performance , applying that caused 1% performance increse (f1score)
