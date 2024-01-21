●	Introduction
This report presents a comprehensive study aimed at developing an early default prediction model for credit card risk assessment. With the increasing prevalence of credit card usage, financial institutions face significant challenges due to customer defaults. This study seeks to address this critical issue, offering a predictive model that can help in minimizing financial losses caused by bad debts.
Credit card defaults have become a growing concern for financial institutions worldwide. The repercussions of these defaults are not only limited to financial losses but also affect the credit market stability. Our focus is a credit card company in Taiwan, which has experienced considerable financial strain due to customer defaults. This scenario underscores the need for an efficient and accurate prediction model to identify potential default risks early.

●	 Data
For this study, the data has been sourced from a publicly available dataset on Kaggle, titled "Default of Credit Card Clients Dataset" (https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset)
This dataset comprises a comprehensive range of information on credit card clients in Taiwan and is recognized for its depth and reliability. Utilizing this dataset provides a solid foundation for our analysis, allowing for a robust examination of the factors contributing to credit card defaults


●	Data Description
ID: A unique identifier for each client.
LIMIT_BAL: The amount of the given credit (NT dollar), including both individual consumer credit and the client's family (supplementary) credit.
SEX: Gender (1 = male; 2 = female).
EDUCATION: Education level (1 = graduate school; 2 = university; 3 = high school; 4 = others).
MARRIAGE: Marital status (1 = married; 2 = single; 3 = others).
AGE: Age in years.
PAY_0 to PAY_6: Repayment status in September, August, ..., April (scale from -1 to 9, where -1 means pay duly, 1 = payment delay for one month, 2 = payment delay for two months, ..., 9 = payment delay for nine months and above).
BILL_AMT1 to BILL_AMT6: Amount of bill statement (NT dollar) from September to April (BILL_AMT1 = amount of bill statement in September, BILL_AMT2 = amount in August, ..., BILL_AMT6 = amount in April).
PAY_AMT1 to PAY_AMT6: Amount of previous payment (NT dollar) from September to April (PAY_AMT1 = amount paid in September, PAY_AMT2 = amount paid in August, ..., PAY_AMT6 = amount paid in April).
default.payment.next.month: Default payment (1 = yes, 0 = no), a binary variable indicating whether or not a client defaulted on the next month’s payment.

●	 Basic stats 
Count: The dataset contains 30,000 entries.
Mean and Standard Deviation (Std):
LIMIT_BAL: The average credit limit is approximately 167,484 with a standard deviation of 129,748.
AGE: The average age of the clients is about 35.5 years with a standard deviation of 9.22 years.
Minimum (Min) and Maximum (Max) Values:
LIMIT_BAL: The credit limit ranges from 10,000 to 1,000,000.
AGE: The age of clients ranges from 21 to 79 years.
25th, 50th (Median), and 75th Percentiles:

LIMIT_BAL: The 25th, 50th, and 75th percentiles are 50,000, 140,000, and 240,000, respectively.
AGE: The corresponding percentiles for age are 28, 34, and 41 years.
PAY_X (X from 0 to 6): These columns represent the repayment status in different months. They have values ranging typically from -2 to 8, indicating different statuses of payment delays.
BILL_AMT_X (X from 1 to 6): These columns indicate the bill amount for different months. The values vary widely, indicating diverse billing amounts across clients.
PAY_AMT_X (X from 1 to 6): These columns show the amount paid in previous months. There is a significant variation in these amounts, as indicated by their standard deviations.
Default Payment Next Month: About 22.12% of the clients are marked as defaulters for the next month.

●	Implications/recommendations for business:
Since both Random forest and XGBoost have the same results and are consistent, we have done more analysis on resource, Interpretability and complexity, and we recommend Random Forest Model considering the size and limited resource of the company to predict the potential payment defaults before they approve the credit cards. On the basis of data, they can also provide small limit balances to the potentially risky customers. 
