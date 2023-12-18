### Project Overview
The objective of this project is to create an effective machine-learning model capable of accurately classifying emails into either spam or non-spam categories.

### Dataset
The dataset utilized for this project comprises a collection of emails, each labeled as either "spam" or "non-spam." The dataset, which contains 4601 records, is available here. Each record represents a distinct email message characterized by 58 attributes. Attributes 1-57 capture various content-based characteristics extracted from the email messages, such as word frequency, punctuation usage, and capitalization. The final attribute represents the class label (spam or non-spam).

### Requirements
To execute the code in this project, the following Python packages are required:

numpy

pandas

scikit-learn

lightgbm

xgboost

scikitplot

matplotlib

seaborn

### Model Evaluation
The model's performance is assessed using metrics such as accuracy, precision, recall, and F1-score.

### Conclusion

#### Standard Model:

A range of base models, including Naive Bayes, Logistic Regression, KNN, SVM, Random Forest, LightGBM, and Xgboost, are evaluated using RandomizedSearchCV.
LightGBM demonstrates superior predictive performance with an accuracy score and AUC exceeding 95.5% and 98.5%, respectively.
Stacking these fine-tuned base models with Logistic Regression as the final meta-model further improves metrics to over 99%.
Cost-sensitive Model:

A similar approach is followed for the cost-sensitive model, with adjustments made to the class_weight parameter and a custom cost function to consider misclassification costs.
While the cost-sensitive model does not match the general model's predictive power, it delivers good overall performance with accuracy, precision, recall, and F-measure surpassing 90%.
The cost-sensitive model achieves significantly lower total cost compared to the general model (cost-sensitive cost: 114 vs general model cost: 212, based on the confusion matrix).
In summary, both models showcase robust performance, with the cost-sensitive model demonstrating the ability to minimize total misclassification cost-effectively.





