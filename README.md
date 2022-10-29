# Employee churn prediction
Hiring and retaining employees are extremely complex tasks that require time , capital and skills. Companies spend 15-20% of the employee’s salary to recruit a new candidate.
The dataset provided in this case study is collected by HR and provided to analyse and build a strong predictive model to reduce the employee attrition.


# Observations:
1.  On plotting histogram it was observed that there were some features like MonthlyIncome, TotalWorkingYears, YearsSinceLastPromotion and YearsAtCompany had a long tailed distribution which means there were some employees who were outliers falling into the high range of these categories.
    
2.  Performed outlier detection and treatment on MonthlyIncome by replacing the last 10 percentile with the median MonthlyIncome.
    
3.  On plotting heatmap it was observed that there are several features which are mostly giving intuition of employees either being at high post in the company or associated with the company for longer duration had low attrition rate compared to new and young employees.
    
4.  Sales representative seemed to be the lowest paid employees and they have the highest churning rate among all other job role.
    
5.  Dataset contains many categorical columns , performed one hot encoding to convert them into numerical columns before feeding them to Machine learning model.
    
6.  Build Logistic Regression model using class_weight to deal with imbalanced dataset using regularization parameter C = 0.1 (Found using GridSearchCV) and achieved following metrics on test data.
   

	|| Metric |Value  | 
	|--|--|--|
	|| Accuracy | 0.86 | 
	|| ROC_AUC | 0.73 | 
	|| Precision | 0.55 | 
	|| Recall | 0.55 | 


    

7.  Used Neural Network with just 3 hidden layers with 500 neurons in each layer and ‘relu’ as the activation function, received following metrics.
	|| Metric |Value  | 
	|--|--|--|
	|| Accuracy | 0.85 | 
	|| ROC_AUC | 0.68 | 
	|| Precision | 0.52 | 
	|| Recall | 0.48 | 
    

    

8.  Used Lazy Predict to apply 25 ML algorithms to get an overview of which works best for the given dataset. It was observed that boosting algorithms are performing very well here.
    
9.  Metrics with Adaboost:
	|| Metric |Value  | 
	|--|--|--|
	|| Accuracy | 0.88 | 
	|| ROC_AUC | 0.69 | 
	|| Precision | 0.69 | 
	|| Recall | 0.43 |  
