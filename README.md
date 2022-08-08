# Credit Risk Analysis

## Overview
### Purpose
The purpose of this analysis is to compare different sampling techniques and machine learning models on a credit risk dataset. Credit risk datasets require techniques to counter bias since the number of good loans far exceeds the number of risky loans. I tested the Random Over Sampler and SMOTE algorithms for oversampling, the Cluster Centroids algorithm for undersampling, and the SMOTEENN algorithm for a combination approach. With each of these sampling techniques I used a logistic regression model to classify credit risk as low or high risk. Then I tested the Balanced Random Forest Classifier and Easy Ensemble Classifier models that reduce bias. I compared the accuracy scores, confusion matrices, and classification reports of all of these methods to determine the best machine learning method for classifying credit risk with an unbalanced dataset.

## Results
### Random Over Sampler
- The balanced accuracy score was 66.1%.
- The precision of high-risk classification was 0.01 and the precision of low-risk classification was 1.00. Therefore, the low-risk classifications are extremely reliable while the high-risk classifications are extremely unreliable.
- The recall of high-risk classification was 0.72 and the recall of low-risk classification was 0.60. Therefore, the high-risk classification has greater sensitivity than the low-risk classification. The model correctly identified 72% of all high-risk cases.
![image](https://user-images.githubusercontent.com/102445183/183317097-737f7d7c-f3bb-430f-8eb5-f21202842562.png)

### SMOTE
- The balanced accuracy score was 65.8%.
- The precision of high-risk classification was 0.01 and the precision of low-risk classification was 1.00. Therefore, the low-risk classifications are extremely reliable while the high-risk classifications are extremely unreliable.
- The recall of high-risk classification was 0.63 and the recall of low-risk classification was 0.68. Both recall scores are fairly low. The model correctly identified 63% of all high-risk cases.
![image](https://user-images.githubusercontent.com/102445183/183318164-e8019513-240a-4087-b06c-d7713812e95b.png)

### Cluster Centroids
- The balanced accuracy score was 54.4%. This is the lowest accuracy of all methods tested.
- The precision of high-risk classification was 0.01 and the precision of low-risk classification was 1.00. Therefore, the low-risk classifications are extremely reliable while the high-risk classifications are extremely unreliable.
- The recall of high-risk classification was 0.69 and the recall of low-risk classification was 0.40. Therefore, the high-risk classification has greater sensitivity than the low-risk classification. The model correctly identified 69% of all high-risk cases.
![image](https://user-images.githubusercontent.com/102445183/183318249-ebacd3d0-c16e-4c1a-a12b-109b3ba75208.png)

### SMOTEENN
- The balanced accuracy score was 64.8%.
- The precision of high-risk classification was 0.01 and the precision of low-risk classification was 1.00. Therefore, the low-risk classifications are extremely reliable while the high-risk classifications are extremely unreliable.
- The recall of high-risk classification was 0.72 and the recall of low-risk classification was 0.57. Therefore, the high-risk classification has greater sensitivity than the low-risk classification. The model correctly identified 72% of all high-risk cases.
![image](https://user-images.githubusercontent.com/102445183/183318284-03f9dbf7-923d-4d7e-a20d-6939d3275916.png)

### Balanced Random Forest Classifier
- The balanced accuracy score was 78.8%.
- The precision of high-risk classification was 0.03 and the precision of low-risk classification was 1.00. Therefore, the low-risk classifications are extremely reliable while the high-risk classifications are extremely unreliable.
- The recall of high-risk classification was 0.70 and the recall of low-risk classification was 0.87. Therefore, the high-risk classification has lower sensitivity than the low-risk classification. The model correctly identified 70% of all high-risk cases.
![image](https://user-images.githubusercontent.com/102445183/183318428-120baa17-4e16-40a7-9b08-0de06e28f003.png)

### Easy Ensemble Classifier
- The balanced accuracy score was 93.2%. This is the highest accuracy of all methods tested.
- The precision of high-risk classification was 0.09 and the precision of low-risk classification was 1.00. Therefore, the low-risk classifications are extremely reliable while the high-risk classifications are extremely unreliable.
- The recall of high-risk classification was 0.92 and the recall of low-risk classification was 0.94. Both recall scores are very high. The model correctly identified 92% of all high-risk cases.
![image](https://user-images.githubusercontent.com/102445183/183319128-3a9d320a-54aa-45ba-9e30-55484b9dfb07.png)

## Summary
### Summary of results
The two machine learning models both showed better results at reducing bias than any of the resampling algorithms. The resampling algorithms all performed similarly, with accuracy scores of around 65%, except for the Cluster Centroids undersampling algorithm which performed the worst with an accuracy of 54.4%. The resampling algorithms also all showed high-risk classification recall scores of about 0.65-0.70. The Easy Enseble Classifier performed with the highest balanced accuracy score, 93.2%, and the highest high-risk classification recall, 0.92.

### Recommendations
It is clear that the Easy Ensemble Classifier is the right model to use to analyse the credit risk data, as it showed a very high accuracy score and a very high high-risk classification recall score. The recall score for high-risk loans is the most important for reducing risk since identifying as many high-risk loans as possible will reduce the amount of bad loan agreements that are accepted.
