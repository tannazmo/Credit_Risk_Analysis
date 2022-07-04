# Credit Risk Analysis


## Overview of the loan prediction risk analysis:

This analysis is done to find the best possible machine learning model that detects the credit applicants that might default on their payments.

## Results: 

In this analysis we have implemented six machine learning models:
- Naive Random Over-Sampling
- SMOTE Over-Sampling
- Cluster Centroid Under-Sampling
- SMOTEENN (Combination of over and under sampling algorithm)
- Balanced Random Forest Classifier
- Easy Ensemble AdaBoost Classifier

For each of these models, we have calculated their performance metrics such as:
- Balanced Accuracy Score
- Precision
- Recall 

#### Naive Random Over-Sampling:
The metrics of this model as shown below, suggests that this model is not the best in detecting high credit risks as the precision for high risks is 0.01%. but recall for high risks is at 69% and balanced accuracy score is about 64%.

![Random_Over_Sampling](/images/Naive_Random_Oversampling.png "Random Over Sampling")

#### SMOTE
The same metrics in this model as shown below, has not made much improvement, as the sensitivity at 0.60 is even lower for high-risk in this model compared to the random over-sampling and the balanced accuracy score has improved very little to about 65%.

![SMOTE](/images/SMOTE.png "SMOTE")

#### Cluster Centroid Under-Sampling
By using the Cluster Centroid under sampling model, even though it is doing a little better in sensitivity to high risk, in comparison to SMOTE, but overall recall is at 40% which is not the best and balanced accuracy score has dropped to 54%.

![Cluster_Centroid_Under_Sampling](/images/Undersampling.png "Cluster-Centroid Under-Sampling")

#### SMOTEENN (Combination of over and under sampling algorithm)
This time, we used SMOTEENN or a combination of oversampling and under sampling as combined methods, may improve the results. and the metrics below, shows that this model is a little better than CC-Undersampling and SMOTE, but very similar to Random OverSampling as recall for high risk is at 69% and recall for low-risk is at 58% and the precision has remained unchanged in all of our models used so far which is about 1% for high-risk and 99% for low-risk and balanced accuracy score is still at about 64%

![SMOTEENN](/images/SMOTEENN.png "SMOTEENN")

#### Balanced Random Forest Classifier
This time we have used an ensemble method, that is known to improve the performance metrics. With the Balanced Random Forest Classifier, we were able to get 70% sensitivity for the high-risk and even the precision for high risk went a bit higher too and with the balanced accuracy score of about 79%, this model has proved to be the best of them so far.

![Balanced_Random_Forest_Classifier](/images/Balanced_Random_Forest.png "Balanced Random-Forest Classifier")

#### Easy Ensemble AdaBoost Classifier
The last model we used is another ensemble method, called Easy Ensemble Adaboost classifier and as shown in the image below, the precision for high risk has improved a little more, but the best improvement is seen on the sensitivity (which in the case of credit risk prediction, is a more important metric to look at), that has jumped to a total 94% and specifically for high-risk is about 92% which is a great improbement in comparison to non-ensemble methods. For this method, we also can see a balanced accuracy score of 93% which is the best among the six models used. 

![Easy_Ensemble_Classifier](/images/Easy_Ensemble.png "Easy_Ensemble_Classifier")


## Summary

Looking at all the metrics of the six algorithms that we used for this dataset, we can clearly see that Easy Ensemble Adaboost Classifier performed best among these six models with 92% on recall for high-risk credits, we can be confident that this model detects almost all the credit risks.
