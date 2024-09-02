# BCG PowerCo Churn Analysis



### **Overall Purpose**

The **BCG PowerCo Churn Analysis** is a project designed to predict customer churn for PowerCo. The goal is to help the company identify customers who are likely to leave (churn), enabling the implementation of targeted retention strategies.

However, the main objective of this project is to test the hypothesis that price sensitivity is a major contributing factor to customer churn.

### **Exploratory Data Analysis Findings**

- Total customer churn for PowerCo is about 10%.
- Churning is distributed among five channel sales features.
- Consumption data and forecasts are highly positively skewed.

### **New Features Created and Some Transformations**

- Difference between off-peak prices in December and the preceding January.
- Average price change across periods.
- Max price changes across periods.
- Tenure feature—how long a company has been a PowerCo client.
- Transforming dates into months to get a numerical value associated with contract duration.
- Creating new features based on correlation and dropping less correlating ones.

### Modeling and Observations

Using RandomForrest Classifier has given below results:
True positives: 20
False positives: 4
True negatives: 3282
False negatives: 346

Accuracy: 0.9041621029572837(90%)
Precision: 0.8333333333333334
Recall: 0.0546448087431694

**Note**:Scores can varry a little after each execution cycle of code.

Although the model's accuracy is good at predicting true negatives, the overall accuracy for true positives is poor due to a class imbalance in the churn feature. However, this model allows us to address our main hypothesis through the important_features_ factor.

Since price features are scattered throughout the important_features_ factor and not concentrated at the top, price sensitivity is not a major factor in predicting churn. Instead, net margin and consumption are the primary drivers of churn. Other influential factors include the margin on power subscriptions and the duration of customers' previous contracts with PowerCo.