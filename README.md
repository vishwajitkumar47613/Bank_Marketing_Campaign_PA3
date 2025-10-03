# Practical Application III: Comparing Classifiers

## Overview

In this practical application, we aim to **compare the performance** of several supervised machine learning classifiers on a real-world dataset. The classifiers used in this analysis are:

- K Nearest Neighbors (KNN)
- Logistic Regression
- Decision Trees
- Support Vector Machines (SVM)

We utilize a dataset related to **marketing bank products over the telephone**, sourced from the UCI Machine Learning Repository.

## Dataset

The data is from a **Portuguese banking institution** and contains information about the results of various direct marketing campaigns. The goal is to predict whether a client will subscribe to a term deposit based on their attributes and past interactions.

-  Source: [UCI Machine Learning Repository - Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)
-   More info: [Related research article (Moro et al., 2014)](https://www.sciencedirect.com/science/article/pii/S0957417414001166)

## Results Summary

The table below summarizes the training time, accuracy, recall scores, and best cross-validation performance for each classifier:

| Model                   | Train Time (s) | Train Accuracy | Test Accuracy | Train Recall | Test Recall | Best CV Accuracy | Best CV Recall |
|------------------------|----------------|----------------|----------------|---------------|--------------|------------------|----------------|
| KNeighborsClassifier   | 3.63           | 1.0000         | 0.8973         | 1.0000        | 0.3707       | 0.8880           | 0.3384         |
| LogisticRegression     | 1.87           | 0.8592         | 0.8654         | 0.8855        | 0.9116       | 0.8589           | 0.8790         |
| DecisionTreeClassifier | 1.38           | 0.9374         | 0.9142         | 0.6307        | 0.5183       | 0.9077           | 0.5213         |
| SVC                    | 672.28         | 0.8475         | 0.8485         | 0.9119        | 0.9267       | 0.8469           | 0.9089         |

## Key Takeaways

- **Support Vector Machine (SVM)** achieved the highest **test recall** (0.9267) and strong **cross-validation recall** (0.9089), making it highly effective for identifying positive cases — but at a significant **computational cost** (672s).
- **Logistic Regression** offered an excellent **balance of recall (0.9116)**, good **accuracy**, and very **low training time**, making it a highly efficient and practical model.
- **Decision Tree** showed strong **test accuracy (0.9142)** and **cross-validation accuracy (0.9077)**, but recall was moderate, which may limit its usefulness in recall-critical applications.
- **K-Nearest Neighbors (KNN)** achieved perfect training metrics (1.0000) but **poor test recall (0.3707)**, suggesting it may be overfitting and not generalizing well.
- **Improving Model** Recall can be improved for Logistic Regression, KNN but comes at a cost of precision.We have to find the right balance here.
