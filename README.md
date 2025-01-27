# Reducing Customer Churn <br> Using Machine Learning to Predict Customer Retention at Syriatel- A telecommunication Company

![Churn](churn.png)
## PROJECT OVERVIEW
Customer churn, also known as customer attrition or customer turnover, refers to the rate at which customers stop doing business with a company over a given period of time. It is a crucial metric for businesses, especially those in subscription-based industries or services, as it directly impacts the company's revenue and growth.
This project sets out to Investigate and analyze factors influencing customer churn in Syriatel - a telecommunication company, using a comprehensive dataset from Kaggle. The project aims to identify patterns and key drivers of customer attrition, providing actionable insights and strategic recommendations to aid Syriatel's decision-makers in implementing effective customer retention strategies.

## BUSINESS UNDERSTANDING
In the fiercely competitive telecommunications industry, Syriatel Communications aims to tackle the challenge of customer churn through a proactive and data-driven approach. The objective is to develop a predictive model that identifies potential churners, allowing the implementation of targeted strategies for customer retention and overall business growth.

The benefits are clear: by reducing churn rates, Syriatel anticipates increased revenues, profitability, and market positioning. Customers will enjoy improved services and tailored offerings, while shareholders can expect enhanced returns on their investments. Employees, too, stand to gain through better remuneration and a thriving work environment as the company continues to succeed.

This initiative underscores Syriatel's commitment to innovation, customer satisfaction, and sustained growth, positioning it as a leader in the dynamic telecommunications landscape. Through strategic predictive analytics, the aim is not only to minimize churn but also to create lasting value for all stakeholders.

## SPECIFIC OBJECTIVES:
To identify the key features that determine if a customer is likely to churn.

To determine the most suitable model to predict Customer Churn.

To establish Cusstomer retention strategy to reduce churn


## DATA UNDERSTANDING
The data is sourced from Kaggle and contains comprensive information about syriatel customers including whether they terminated their subscriptions with the company or not. 
The dataset contains 3333 entries and 21 columns. 

#### Summary of Features in the Datset

- **State**: *The state the customer lives in*
- **Account Length:** *The number of days the customer has had an account.*
- **Area Code:** *The area code of the customer*
- **Phone Number:** *The phone number of the customer*
- **International Plan:** *True if the customer has the international plan, otherwise false.*
- **Voice Mail Plan:** *True if the customer has the voice mail plan, otherwise false.*
- **Number Vmail Messages:** *the number of voicemails the customer has sent.*
- **Total Day Minutes:** *total number of minutes the customer has been in calls during the day.*
- **Total Day Calls:** *total number of calls the user has done during the day.*
- **Total Day Charge:** *total amount of money the customer was charged by the Telecom company for calls during the day.*
- **Total Eve Minutes:** *total number of minutes the customer has been in calls during the evening.*
- **Total Eve Calls:** *total number of calls the customer has done during the evening.*
- **Total Eve Charge:** *total amount of money the customer was charged by the Telecom company for calls during the evening.*
- **Total Night Minutes:** *total number of minutes the customer has been in calls during the night.*
- **Total Night Calls:** *total number of calls the customer has done during the night.*
- **Total Night Charge:** *total amount of money the customer was charged by the Telecom company for calls during the night.*
- **Total Intl Minutes:** *total number of minutes the user has been in international calls.*
- **Total Intl Calls:** *total number of international calls the customer has done.*
- **Total Intl Charge:** *total amount of money the customer was charged by the Telecom company for international calls.*
- **Customer Service Calls:** *number of calls the customer has made to customer service.*
- **Churn:** *true if the customer terminated their contract, otherwise false*

#### TARGET VARIABLE
![Target](TARGET.png)

#### Relationship between some key features:
![correlations](correlations.png)

## MODELING
In order to come up with a predictive model that will be used in evaluating a customer's propensity to churn, an iterative approach to modelling was employed where a total of six classifiers were fitted and evaluated
The six classifiers were compared and the best performing classifiers on the basis of AUC scores was identified and the best predictive model
#### Vanilla Logistic Regression Classifier
As a baseline model, a vanilla Logistic regression model was fitted and evaluated, where the following classification metrics were recorded
![Logistic_ROC](Rogreg_roc.png)
The performance on Training and Testing:-<br>
- Training Precision = 0.5523809523809524
- Training recall = 0.15977961432506887
- Training F1 Score = 0.24786324786324784
   
- Testing Precision = 0.4642857142857143<br>
- Testing Recall =  0.10833333333333334<br>
- Training F1 Score = 0.17567567567567569 <br>

#### Decision Tree Classifier
PERFORMANCE:
- Precision on training = 0.7195767195767195 <br>
- Recall on Training = 0.3746556473829201 <br>
- F1 Score on Training = 0.4927536231884058<br>

- Precision on testing = 0.6842105263157895 <br>
- Recall on Testing = 0.325 <br>
- F1 Score on Testing = 0.4406779661016949<br>

#### Random Forest Classifier
PERFORMANCE:
- Random forest Training Precision = 0.8641975308641975 <br
- Random forest Training Recall = 0.1928374655647383<br>
- Random forest Training f1_Score = 0.31531531531531526<br>

#### Gradient Boosting: XGBoost Classifier
PERFORMANCE
- XGBoost Training Precision =  1.0 <br>
- XGBoost Training Recall =  0.8402203856749312<br>
- XGBoost Training f1_score =  0.9131736526946108<br>

#### FEATURE IMPORTANCES
![Feature importances](feature_importances.png)
### MODEL COMPARISONS
![Model Comparisons](comparisons.png)
Comparing the AUC for all the models, we establish that the Random Forest Classifier had the highest (AUC = 0.79) and best classification performance. Therefore Random Forest was chosen as the most efficient model for the classification task at hand!
## Conclusions & Recommendations
In summary, the analysis indicates a high level of accuracy in predicting customer churn through the application of machine learning techniques. The Random Forest Classifier emerges as the recommended model, showcasing superior overall performance. Its ROC curve gracefully aligns with the upper left corner of the graph, resulting in the largest Area Under the Curve (AUC).

The study Recommend adopting Random Forest Classifier as the primary model for predicting customer churn.-<br>
#### Business Strategic Recommendations for SyriaTel:
Implement a targeted Customer Retention stratety
- Focus on key features related to call minutes and charges.
- Consider personalized offers or discounts on daily charges.
- Aim to retain customers and minimize potential revenue loss.
Address factors contributing to Customer Churn:
- Develop strategies to reduce customer service calls.
- Enhance customer experience and satisfaction.
