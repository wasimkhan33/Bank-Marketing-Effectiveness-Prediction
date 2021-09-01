# Bank_Marketing_Effectiveness_Prediction

Colab Notebook link - https://colab.research.google.com/drive/1IQU4niWC_4xkU3WXp2P3ZkbzwFZx1rHn?usp=sharing

## Problem Description
The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed. The classification goal is to predict if the client will subscribe a term deposit (variable y)

## Bank Client data:
age (numeric)

job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')

marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)

education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')

default: has credit in default? (categorical: 'no','yes','unknown')

housing: has housing loan? (categorical: 'no','yes','unknown')

loan: has personal loan? (categorical: 'no','yes','unknown')

## Related with the last contact of the current campaign:
contact: contact communication type (categorical: 'cellular','telephone')

month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')

day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')

duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.

## Other attributes: 
campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)

pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)

previous: number of contacts performed before this campaign and for this client (numeric)

poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

## Output variable (desired target):
y - has the client subscribed a term deposit? (binary: 'yes','no')

## Short Summary of your Capstone project and its components. Describe the problem statement, your approaches and your conclusions. 
Completed capstone project 3 on Bank Marketing Effectiveness Prediction using a supervised machine learning classification model where the classification goal is to predict if the client will subscribe to a term deposit (variable y) in direct marketing campaigns (phone calls) of a Portuguese banking institution. And after doing this analysis that I get to know that people with Secondary education qualifications and blue-collar jobs have subscribed more for the deposits than people with any other qualification and profession. Married people and those who were contacted on cellular by the bank have subscribed more to the term deposits than people with any other marital status and contact type. The month of the highest level of marketing activity was the month of May, it was also the month that potential clients tended to reject term deposit offers the most. People with default status as no are the most one’s who have and have not subscribed for bank deposits. People with no housing loan and with a personal loan are the most ones who have subscribed for deposits, and many people whose previous outcome is non-existent have subscribed more than any other group of people belonging to the previous outcome. The average subscription rate tends to be higher for customers below 20-25 years old or above 59 years old. Also, we had observed that potential clients on average and high balances are more likely to open a term deposit and the Client shows interest on deposits who discussed a longer duration (50-60 min.). Lastly, the average subscription rate is below 50% if the number of contacts during the campaign exceeds 4.

Also, we found that the Target variable in our dataset is highly imbalanced, so we had used the random oversampling technique. It duplicates the existing data points of minority class and equalizes the ratio of majority and minority class. Then we had done modelling using the ML classification model. 
Among the three classification approach used to model the data, we found that Accuracy and AUC ROC score is high for almost all models whether it is for balanced or Imbalance dataset.

•	Random Forest with balance dataset contain high AUC ROC score.

•	Random Forest and Knn with Imbalance set both contain high Accuracy.

•	But for fair model performance among all balance and Imbalance datasets, we decided the best model using F1 Score here also Random Forest in balance dataset is the best model.

•	And also when we talk about only Balance data set comparison, Random Forest is the best model in all Evaluation metrics.

## Proposed solutions for the Next Marketing Campaign :
Months of Marketing Activity: For the next marketing campaign, it will be wise for the bank to focus the marketing campaign during the months of March, September, October, and December. (December should be under consideration because it was the month with the lowest marketing activity, there might be a reason why December is the lowest.)

Campaign Calls: A policy should be implemented that states that no more than 3 calls should be applied to the same potential client. Remember, the more we call the same potential client, the higher the likelihood he or she will decline to open a term deposit. This might be as a result of a potential client getting tired/pissed at being disturbed. It also saves us time and effort in getting new potential clients.

Age Category: The customer's age affects campaign outcome as well. The next marketing campaign of the bank should target potential clients in their 20s or younger and 60s or older. This will increase the likelihood of more term deposits subscriptions.

Occupation: Potential clients that were students or retired were the most likely to subscribe to a term deposit. Retired individuals, tend to have more term deposits in order to gain some cash through interest payments. Retired individuals tend to not spend so much of their money as responsibilities are usually reduced, so they are more likely to lend it to the financial institution. Students were the other group that used to subscribe to term deposits.

Balances: We see those potential clients on average and high balances are more likely to open a term deposit. Lastly, the next marketing campaign should focus on individuals of average and high balances in order to increase the likelihood of subscribing to a term deposit as they have more money to spare.

## Final Conclusion
From the study conducted, the results are impressive and convincing in terms of using a machine-learning algorithm to decide on the marketing campaign of the bank. Among the three classification approach used to model the data, we found that Accuracy and AUC ROC score is high for almost all models whether it is for balanced or Imbalance dataset.

Random Forest with balance set is highest with 93% of AUC ROC score.

Random Forest and Knn with Imbalance set both contain 89% of Accuracy.

But for fair model performance among all balance and Imbalance datasets, we decided the best model using F1 Score here also Random Forest is the clear winner on balance dataset with a score of 86%.

And also when we talk about Balance data set comparison Random Forest is the best model in all Evaluation metrics.

Further, we can also improve using hyper tuning on our Algorithm to get the most out of it but Hyper Tuning consumes a lot of time and resources of the system depending upon how big the Data we have and what algorithm we're using. It will go through a number of Iterations and try to come up with the best possible value for us.

The bank marketing manager can identify the potential client by using the model if the client’s information like education, housing loan, Personal loan, duration of the call, number of contacts performed during this campaign, previous outcomes, etc is available. This will help the bank to predict the success of subscribing to a long-term deposit even before the telemarketing call is executed.

Thank you for your time.
