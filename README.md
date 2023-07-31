# Marketing-Classifier-Comparison

### Overview
The goal of this project is to compare the performance of different classifiers, including K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines, using a Portuguese bank marketing campaign dataset. By analyzing customer features such as demographics and transaction history, we aim to predict customer saving behaviors and identify which types of customers are more likely to make term deposits. This analysis will help the bank optimize its marketing efforts and enhance overall customer satisfaction.

### Background
To succeed in a competitive market, effective marketing strategies are crucial for companies. This dataset contains information about direct phone call marketing campaigns conducted by a Portuguese banking institution from May 2008 to November 2010. Our objective is to predict customer responses to the telemarketing campaign and create a target customer profile for future marketing plans. By analyzing customer attributes, we can identify which customers are more likely to subscribe to term deposits and focus our marketing efforts on them.

### Understanding the Features
The dataset consists of various customer attributes, including age, job type, marital status, education, credit status, housing loan status, contact communication type, and more. The output variable 'y' indicates whether the client subscribed to a term deposit or not.

### Key Insights

### Target Variable Distribution
The dataset is imbalanced, with significantly more 'no' values (36,548) than 'yes' values (4,640) for the target variable 'y'.

### Percentage of each unique value in 'y' column:

<img width="486" alt="Screenshot 2023-07-31 at 12 22 44 AM" src="https://github.com/hdawit/Marketing-Classifier-Comparison/assets/43795941/ddfa1036-2810-4ab0-a59e-71284f71f832">

(Target variable 'y' has two unique values: 'yes' and 'no'. The majority of the customers did not subscribe to a term deposit, as 'no' values constitute the majority.)
Impact of Job Type on Subscriptions

### Subscription Status by Job Type:

<img width="776" alt="Screenshot 2023-07-31 at 12 24 06 AM" src="https://github.com/hdawit/Marketing-Classifier-Comparison/assets/43795941/259c1b04-adcb-42d9-ad03-9982758497e4">

(The highest percentage of "yes" subscriptions is for customers with the job type of "student", followed by "retired" and "unemployed". On the other hand, the lowest percentage of "yes" subscriptions is for customers with the job type of "blue-collar", followed by "services" and "entrepreneur".)
Distribution of Age

### Age Distribution:

<img width="690" alt="Screenshot 2023-07-31 at 12 24 49 AM" src="https://github.com/hdawit/Marketing-Classifier-Comparison/assets/43795941/e5d4d0ef-43cc-4297-9441-7ece1001892a">

(The age distribution is roughly normal with a peak in the late 20s to early 30s.)
Relationship between Duration, Campaign, and Subscription Result

### Duration and Campaign vs. Subscription Result:

<img width="529" alt="Screenshot 2023-07-31 at 12 25 26 AM" src="https://github.com/hdawit/Marketing-Classifier-Comparison/assets/43795941/ecf9fe6d-2e85-4f2d-84d2-e83b9ac60b24">

(The plot shows that the clients who subscribed to a term deposit tended to have longer durations of the last contact and were contacted fewer times during the current campaign compared to those who did not subscribe. This suggests that longer conversations may have had a positive impact on the clients' decision to subscribe.)

### Model Performance Comparison
Based on four performance metrics (accuracy, precision, recall, and F1 score):
•	SVM outperformed other models in accuracy (90.30%), precision (69.24%), and F1 score (46.75%).
•	Decision Trees showed the highest recall (47.48%), meaning it correctly identified actual positive cases.
•	Logistic Regression and KNN also yielded respectable performance.

### Correlation Matrix and Heatmap
The correlation matrix and heatmap revealed insights into the relationships between numerical columns in the dataset. For example, the 'duration' column has a strong positive correlation with the 'balance' column.

### Confusion Matrix Analysis
Each classifier's confusion matrix helped us evaluate its performance:
•	KNN classifier achieved 97% accuracy with a good balance between precision and recall (F1 score: 91%).
•	Logistic Regression showed a higher accuracy in predicting 'no' subscriptions but had a higher number of false positives and negatives.
•	Decision Trees exhibited decent accuracy, but its precision for predicting 'yes' subscriptions was low.
•	SVM classifier achieved high accuracy but struggled to correctly identify positive cases.
### Conclusion
The analysis provided valuable insights into the performance of different classifiers for predicting customer subscriptions. SVM demonstrated the best overall performance, while Decision Trees showed the highest recall. Logistic Regression performed well in terms of accuracy and F1 score. However, hyperparameter tuning and further model optimization could enhance the overall performance of these classifiers.
