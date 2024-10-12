# Heart-Disease-Risk-Prediction

### Summary and Recommendations

#### 1. Overview

The project analyzes customer churn data to determine churn rates over different periods (monthly, quarterly, yearly) and identifies the primary factors contributing to churn. Key factors like contract type, payment method, and internet service are found to significantly impact customer churn. 

Goals:

- Calculate churn rates to understand how many customers are leaving within different time periods (monthly, quarterly, yearly).
- Identify the factors most strongly associated with customer churn, such as contract type, payment method, and internet service.
- Use machine learning to evaluate feature importance and determine which features are most predictive of churn.

#### 3. Data Analysis Steps

1. Initial Data Exploration
2. Data Cleaning
3. Outlier Detection
4. Data Visualization

#### 4. Data Preprocessing

- Handle Missing Values: It converts the Total Charges column to numeric and fills missing values with the median.
- Categorical Encoding: Converts columns like Country, State, City, etc., into categorical data types.
- Binary Encoding: Converts the Senior Citizen column to binary (Yes -> 1, No -> 0).
- Irrelevant Columns Dropped: Removes unnecessary columns like CustomerID, Count, and Lat Long.

#### 5. Data Visualization

- Churn Rate by Contract Type: Customers on month-to-month contracts churn much more frequently than those on longer contracts. This reinforces the idea that locking customers into longer-term commitments reduces churn.
- Churn Rate by Payment Method: Electronic check is a strong indicator of churn, while other automatic payment methods have much lower churn rates. This could be an actionable insight for the company, suggesting they might want to encourage customers to switch to automatic payment methods to reduce churn.

#### 6. Key Findings
      
- Overall Churn Rate: 26.54%.
- Churn Rate by Contract Type: Month-to-month contracts show the highest churn (42.7%), while two-year contracts have the lowest churn (2.8%).
- Churn Rate by Payment Method: Electronic check payments are associated with a much higher churn rate (45.3%) compared to automatic payment methods.
- Churn Rate by Internet Service: Fiber optic customers have the highest churn rate (41.9%), while those with no internet service have the lowest (7.4%).
