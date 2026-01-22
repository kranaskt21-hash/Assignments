# Sampling Assignment – Credit Card Fraud Detection

## Objective
The objective of this assignment is to study the impact of different sampling techniques on the performance of machine learning models when applied to a highly imbalanced dataset.

---

## Dataset
- **Name:** Creditcard_data.csv  
- **Target Variable:** `Class`
  - 0 → Non-Fraud
  - 1 → Fraud

The dataset is highly imbalanced, which makes sampling and balancing techniques essential.

---

## Methodology

### 1. Feature Engineering
To improve data quality and model performance:
- Standard Scaling was applied to normalize the features.
- Principal Component Analysis (PCA) was used to remove redundancy and noise.

---

### 2. Dataset Balancing
The dataset was balanced using **SMOTE-ENN**, which:
- Oversamples the minority class
- Removes noisy samples using Edited Nearest Neighbours

This ensures both classes are sufficiently represented.

---

### 3. Sampling Techniques
After balancing, the following sampling techniques were applied:

1. Simple Random Sampling  
2. Systematic Sampling  
3. Stratified Sampling  
4. Cluster Sampling  
5. Bootstrap Sampling  

---

### 4. Machine Learning Models
The following efficient and popular machine learning models were used:

- Logistic Regression  
- Gradient Boosting  
- Naive Bayes  
- Random Forest  
- K-Nearest Neighbors (KNN)  

---

### 5. Model Evaluation
- Stratified 5-Fold Cross Validation was used.
- Accuracy was chosen as the evaluation metric.
- Stratification preserves class distribution across folds.

---

## Results

* An accuracy comparison table is generated.
* The best sampling technique for each model is identified.
* Ensemble models such as Random Forest and Gradient Boosting show strong performance.

### Final Accuracy Comparison Table

| Model               | Simple Random | Systematic | Stratified | Cluster | Bootstrap |
| ------------------- | ------------- | ---------- | ---------- | ------- | --------- |
| Logistic Regression | 81.39         | 86.63      | 83.97      | 88.89   | 88.33     |
| Gradient Boosting   | 98.63         | 96.91      | 98.46      | 99.69   | 98.83     |
| Naive Bayes         | 82.51         | 80.66      | 81.82      | 85.41   | 83.60     |
| Random Forest       | 97.69         | 98.15      | 97.43      | 99.39   | 98.28     |
| KNN                 | 94.77         | 88.06      | 93.74      | 95.44   | 96.57     |

### Final Result Table

| Model                     | Best Sampling Technique | Accuracy (%) |
| ------------------------- | ----------------------- | ------------ |
| Logistic Regression       | Cluster Sampling        | 88.89        |
| Gradient Boosting         | Cluster Sampling        | 99.69        |
| Naive Bayes               | Cluster Sampling        | 85.41        |
| Random Forest             | Cluster Sampling        | 99.39        |
| K-Nearest Neighbors (KNN) | Bootstrap Sampling      | 96.57        |

---

## Observations

* Feature engineering before sampling improves stability.
* Balanced data prevents model failures due to single-class issues.
* Stratified and Bootstrap sampling preserve class distribution better.
* Sampling strategy significantly affects model accuracy.

---



