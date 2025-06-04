**Understand the business problem:**
Through machine learning and data-driven insights, help the bank to enhance the effectiveness of their marketing campaign.

**Data Preparation & Overview**
Number of records: 41,188
Features: 20 input variables (ategorical and numeric)
Target variable y (subscription: 'yes'/'no')
No missing values reported

**Key Features**
Client attributes: age, job, marital status, education, default status, housing/personal loan status
Campaign attributes: contact type, month,call duration, number of contacts, previous outcomes
Socioeconomic context: employment variation rate, consumer price index, consumer confidence index, euribor 3-month rate, number of employees

**Common feature Categories:** Married, University Degree working in Admin.

**Feature engineering**
One-Hot Encode categorical features

**Baseline accuracy**
Most Frequent Accuracy: 0.89

**Model Comparisons**

Model	Train Time (s)	Train Accuracy	Test Accuracy
0	Logistic Regression	0.3195	0.887	0.888
1	KNN	0.0123	0.891	0.880
2	Decision Tree	0.1513	0.892	0.887
3	SVM	0.0602	0.887	0.888

**Improving model through hyperparameter tuning and grid search**
Best parameters for Decision Tree:
{'criterion': 'entropy', 'max_depth': 5, 'min_samples_leaf': 2, 'min_samples_split': 2}
Best cross-validation accuracy on training set: 0.8868
Test Accuracy with best Decision Tree model: 0.8882

Best parameters for KNN:
{'n_neighbors': 9}
Best cross-validation accuracy on training set: 0.8843
Test Accuracy with best KNN model: 0.8852

Grid Search optimized for Recall for Decision Tree:
Best parameters: {'criterion': 'entropy', 'max_depth': None, 'min_samples_leaf': 1, 'min_samples_split': 2}
Best cross-validation recall on training set: 0.1006
Test Recall with best Decision Tree model (optimized for recall): 0.0943

**Conclusion:**
Targeting: Use predictive modeling to identify high-potential client segments
