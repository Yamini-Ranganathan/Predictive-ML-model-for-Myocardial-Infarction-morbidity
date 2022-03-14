# Predictive-ML-model-for-Myocardial-Infarction-morbidity

# AIM:
The aim of this study is to predict the risk of Death & Severe Complications in hospitalized patients with AMI and compare different classifier models based on high accuracy and sensitivity.
# APPROACH:
# Loading and Data cleaning: Download the data from Myocardial infarction complications Data Set from UCI ML Repository (https://archive.ics.uci.edu/ml/datasets/Myocardial+infarction+complications).
Replace the missing values by mean imputation and the data reprocessing is done by SKLEARN standard scalar.
Selecting input and output components: The dataset contained 1700 rows and 124 columns out of which 2-112 can be used as input data for prediction and possible complications (outputs) are from 113-124 columns. For this study in order to find the mortality and severe complications all input columns (2-112) are used for prediction, which corresponds to by the end of the third day (72 hours) after admission to the hospital. Out of the 12 complications (outputs) are listed only three were chosen for this analysis, 124: Lethal outcome (LET_IS), 121: Chronic heart failure (ZSN), and 118: Pulmonary edema (OTEK_LANC).
EDA & Feature Selection: The correlation between factors is identified using correlation matrix. After checking for imbalance of the data set, SMOTE is used for balancing the dataset. Recursive Feature elimination analysis with 5 Kfold stratified cross validation & random forest classification estimator using sklearn.feature_selection RFECV is performed to get best features that can improve model accuracy & auc-roc score.

# DATA MODELING & PERFORMANCE MEASURE
The 10 classifier models used for comparison are Logistic Regression, Random Forest Classifier, SVC, K Neighbors Classifier, Decision Tree Classifier, AdaBoost Classifier, Bagging Classifier, Gradient Boosting Classifier, & a Custom Ensemble method with best and second-best models. With all classifier models a 5 k-Fold Cross-Validation is carried out. The three predicative modes used for comparison are 1. custom ensemble model without SMOTE, 2. custom ensemble model after SMOTE, and 3. custom ensemble model with best features obtained from recursive feature elimination.
The Evaluation metrics used to measure the performance of the classifiers’ models are Accuracy Scores; Confusion Matrix including Precision, Recall, and F1 Score; Log Loss, ROC Curve & AUC score.
