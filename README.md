# AXA Data Science Challenge

**Course:** Machine Learning  
**Instructor:** David Martens  
**Team members:** Ting-Yun Chen, Yifan He, Salma Ahansal, Huiqiu Tang  

*This project cannot be shared publicly due to a confidentiality agreement. If you have any questions about my work or contributions, please feel free to contact me directly.*

---

## Project Overview
This project addresses a business challenge to improve insurance offer conversion rates by predicting customer responses to car insurance offers. The aim is to analyze customer profiles to identify those more likely to accept an offer, ensuring a personalized approach that enhances conversion rates.
### Objectives
1. **Binary Prediction:** Determine whether an offer leads to a contract.
2. **Probability Scores:** Provide prediction scores for test cases, evaluated using the Area Under the Curve (AUC) metric.

## Methodology
### 1. Data Understanding
The dataset includes customer and insurance offer details, with both continuous and categorical variables. Preliminary exploration revealed imbalances in the target variable and issues such as missing values, high cardinality, and correlated features, which were addressed during preprocessing.
### 2. Data Preprocessing
* **Cleaning:** Excluded redundant or incomplete columns and handled missing values using imputation methods.
* **Encoding:** Applied tailored encoding techniques to categorical variables, including dummy encoding and Weight of Evidence (WoE) for high-cardinality features.
* **Outlier Treatment:** Standardized continuous variables and managed extreme values to improve model performance.
* **Splitting:** Divided data into training, validation, and testing subsets (64%, 16%, and 20%, respectively).
### 3. Modeling
Several predictive models were evaluated using grid search for hyperparameter tuning and cross-validation to ensure robustness. The ensemble methods, particularly Random Forest and AdaBoost, demonstrated superior performance.
|Model|Accuracy|AUC|
| ---- | ---- |---- |
|K-Nearest Neighbors|0.6720|0.7053|
|Decision Tree|0.6946|0.7365|
|SVM|0.6733|0.7034|
|Logistic Regression|0.6851|0.7113|
|**Random Forest**|0.7055|**0.7534**|
|AdaBoost|0.7039|0.7520|

The **Random Forest** model was selected as the final model due to its superior AUC score.
### 4. Insights
Feature importance analysis highlighted key factors influencing customer decisions, such as communication frequency, vehicle characteristics, and customer demographics. These findings suggest strategies for targeted offers and improved customer engagement.
### 5. Predictions
The final predictions were generated using the trained model and stored for submission. The results included probability scores for each observation in the test set.

## Conclusion
This project successfully developed a robust predictive framework for assessing insurance offer acceptance. The insights provided serve as a foundation for AXA Belgium to optimize customer interactions and improve conversion rates.