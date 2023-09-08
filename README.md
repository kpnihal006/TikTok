# TikTok
Data analysis of TikTok project (part of Google Advanced Data Analytics Certification)
This project is completed as a part of the Google Advanced Data Analytics Capstone Project.
It utilizes data analytics concepts and techniques covered in the professional certification course.

## Overview
TikTok is a fictitious company created for educational purposes only and any reference is coincidental.
TikTok is a social media company where users upload videos for others to view, like and share. The company is
facing an issue with the large number of claim reports over videos by users. They would like to determine if a video
is a claim or an opinion. The TikTok data teamhave provided us with the dataset having the information of the videos and the reports.

## Objectives
- Predict whether a video contains a claim or it offers an opinion
- Provide insights into the data
- Assess probable relationships between features of the dataset
- Determine factors influencing a claim or an opinion
- Build a machine learning model for the predictions

## Analysis
A PACE strategy document was formulated to initiate the process and workflow.
An initial exploratory data analysis was conducted and the dataset was cleaned and structured for modelling.
There is a near equal balance of opinions and claims in the dataset. Null values are removed.
There is an uneven distribution in video view, like and comment counts. It is highly right-skewed.
There was a difference in video view count between verified and unverified accounts.
Longer video lengths tend to be associated with higher odds of the user being verified.
Visualizations on tableau provided us with a better understanding of the data.
A machine learning model was built to determine if a video contained a claim or offers an opinion,
using different methods such as Random Forest Classification,
Logistic Regression, Extreme Gradient Boosting and Decision Tree Classifier.

## Results
The results of the analysis were as follows:
- A model was built on recall score showed a good success of prediction.
- Primary predictors were related to video engagement levels such as views, likes and comments.
- Video length and verification status of users were factors influencing the classification.

## Solutions
Proposed solutions are as follows :
- Further evaluation using additional user data before deployment
- Monitoring video engagement levels to maintain robustness of model
- Beta testing of the model is recommended to gain better insights and feedback

The results of the models are shown in the jupyter notebook, a brief overview of the scores of each model is given below :
**XGBoost Model**
|      Feature  | precision |  recall  |  f1-score  |  support  |
| ------------- | --------- | -------- | ---------- | --------- |
|     opinion   |    0.99   |   1.00   |    0.99    |   1892    |
|      claim    |    1.00   |   0.99   |    0.99    |   1925    |
|    accuracy   |           |          |    0.99    |   3817    |
|   macro avg   |    0.99   |   0.99   |    0.99    |   3817    |
| weighted avg  |    0.99   |   0.99   |    0.99    |   3817    |

**Random Forest Model**

|      Feature  | precision |  recall  |  f1-score  |  support  |
| ------------- | --------- | -------- | ---------- | --------- |
|     opinion   |    1.00   |   1.00   |    1.00    |   1892    |
|      claim    |    1.00   |   1.00   |    1.00    |   1925    |
|    accuracy   |           |          |    1.00    |   3817    |
|   macro avg   |    1.00   |   1.00   |    1.00    |   3817    |
| weighted avg  |    1.00   |   1.00   |    1.00    |   3817    |

_The models show high accuracy, precision, recall and f1 due to very low misclassification. The score will decrease on an unseen test data._

**NOTE : Visualizations and charts can be found in the jupyter notebooks and executive summaries of each phase in the PACE strategy lifecycle.**

## Libraries Used
- numpy
- pandas
- sklearn
- xgboost
- matplotlib
- seaborn
