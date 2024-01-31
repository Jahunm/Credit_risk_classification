#    Credit Risk Classification 

![credit score](Images/12-5-challenge-image.png)

# **Module 12 Challenge Report**

## *Overview of the Analysis*

The objective of this analysis was to construct a machine learning model capable of determining the creditworthiness of borrowers. We utilized a dataset containing historical lending activity from a peer-to-peer lending services company. The dataset included financial information about the borrowers and the status of their loans. Our target variable was loan_status, which signifies whether a loan is healthy (0) or high-risk (1).

The analysis involved several stages:

- Splitting the data into training and testing sets.
- Creating a logistic regression model using the original data.
- Predicting with a logistic regression model using resampled training data via the RandomOverSampler method from the imbalanced-learn library.

## **Results**
The results of the machine learning models are as follows:

1. Machine Learning Model 1 - Logistic Regression with Original Data:

    - Accuracy: 99%

    - Precision: 
        - Low_risk: 100%
        - High_risk: 85%

    - Recall: 
        - Low_risk: 99%
        - High_risk: 91%

 2. Machine Learning Model 2 - Logistic Regression with Resampled Data:

    - Accuracy: 99%

    - Precision: 
        - Low_risk: 100%
        - High_risk: 84%
    
    - Recall: 
        - Low_risk: 99%
        - High_risk: 99%


## **Summary**
Both models demonstrated strengths and weaknesses. The model trained on original data may be more effective in predicting healthy loans, while the model trained on resampled data may be better at predicting high-risk loans. The choice between models depends on the specific problem at hand. If the priority is to predict high-risk loans (1s), the model with resampled data may be preferred. However, if overall accuracy is paramount, the model with original data may be the better choice.

While both models achieved an accuracy of 99%, the model trained on resampled data demonstrated superior recall scores, with both low-risk and high-risk categories scoring 99%. This is significantly higher than the 91% recall score for high-risk loans in the model trained on original data.

*Given these results, I would recommend the use of the model trained on resampled data (RandomOverSampler) for a financial institution prioritizing the accurate prediction of high-risk loans.*


**File:** [credit_classification](credit_risk_resampling.ipynb)
