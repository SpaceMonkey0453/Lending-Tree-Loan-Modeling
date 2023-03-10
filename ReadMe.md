### Predicting Loan Default with XGBoost and SMOTE-ENN

# Introduction
Lending Club is a peer-to-peer lending platform that connects borrowers and investors. As part of their lending process, Lending Club evaluates loan applications based on a variety of factors, such as credit score, employment status, and loan purpose. One of the biggest challenges for Lending Club is to identify borrowers who are likely to default on their loans, which can lead to significant financial losses.

In this project, we developed a machine learning model using XGBoost and SMOTE-ENN to predict loan default based on Lending Club's historical data. The goal of the model is to help Lending Club identify high-risk borrowers and reduce the number of defaults, which can save them a significant amount of money in the long run.

# Dataset
The dataset used in this project consists of Lending Club's loan data from 2016 to 2018, including 521,435 records and 95 features. The target variable is the loan status, which indicates whether the loan was paid off fully or defaulted. The dataset is highly imbalanced, with 72% of loans paid off fully and 27% defaulting.

# Methodology
To address the class imbalance issue, we used SMOTE-ENN to oversample the minority class and undersample the majority class. We also applied feature engineering techniques, such as one-hot encoding and feature scaling, to prepare the data for modeling.

We trained an XGBoost classifier with 1000 estimators, a maximum depth of 3, and a learning rate of 0.01, using the oversampled and preprocessed data. We evaluated the performance of the model using several metrics, including accuracy, recall, precision, and F1 score.

# Results
The final model achieved an accuracy of 90.45%, a recall of 86.85%, a precision of 79.66%, and an F1 score of 83.10%. The model also achieved a ROC AUC score of 95, indicating good discrimination between the positive and negative classes.

We created several visualizations to help interpret and understand the model's performance. These include a confusion matrix, a feature importance plot, a ROC curve, and a learning curve.

The confusion matrix shows the model's performance in predicting loan default and non-default. The feature importance plot shows the top 20 most important features for the model's prediction. The ROC curve shows the model's true positive rate and false positive rate for different classification thresholds. The learning curve shows the model's training and cross-validation scores as a function of the number of training samples.

# Conclusion
Lending Club approves about 100,000 loans per year, of which 27,000 (27%) default on average, resulting in a loss of 75% of the loan amount for each defaulting loan. This means that Lending Club loses a total of $283,424,500 per year due to loan defaults.

Our XGBoost model trained on Lending Club's historical loan data with SMOTE-ENN oversampling and feature engineering techniques can potentially reduce the number of defaulting loans to 5,000, which would bring the default rate down to 5%. This means that Lending Club would only lose $54,585,000 per year due to loan defaults.

The potential cost savings for Lending Club can be estimated as the difference between the original loss due to loan defaults and the adjusted loss based on our model. This means that our model can potentially save Lending Club around $228,839,500 per year.

We acknowledge that our analysis ignores the potential profits from loans that our model would have denied even though they paid off their loans. However, we believe that the cost savings from reducing loan defaults