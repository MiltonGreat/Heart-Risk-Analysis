# Heart-Disease-Risk-Prediction

### Summary and Recommendations

#### 1. Overview

The goal of this project is to create a Classification Model that can predict whether or not a person has presence of heart disease based on physical features of that person (age,sex, cholesterol, etc.). 

#### 2. Datast

The dataset contains 14 physical attributes based on physical testing of a patient. Blood samples are taken and the patient also conducts a brief exercise test. The "goal" field refers to the presence of heart disease in the patient. It is integer (0 for no presence, 1 for presence). In general, to confirm 100% if a patient has heart disease can be quite an invasive process, so if we can create a model that accurately predicts the likelihood of heart disease, we can help avoid expensive and invasive procedures.

Data dictionary:

- age
- sex
- chest pain type (4 values)
- resting blood pressure
- serum cholestoral in mg/dl
- fasting blood sugar > 120 mg/dl
- resting electrocardiographic results (values 0,1,2)
- maximum heart rate achieved
- exercise induced angina
- oldpeak = ST depression induced by exercise relative to rest
- the slope of the peak exercise ST segment
- number of major vessels (0-3) colored by flourosopy
- thal: 3 = normal; 6 = fixed defect; 7 = reversable defect
- target:0 for no presence of heart disease, 1 for presence of heart disease

Creators: 

Hungarian Institute of Cardiology. Budapest: Andras Janosi, M.D. University Hospital, Zurich, Switzerland: William Steinbrunn, M.D. University Hospital, Basel, Switzerland: Matthias Pfisterer, M.D. V.A. Medical Center, Long Beach and Cleveland Clinic Foundation: Robert Detrano, M.D., Ph.D.

#### 3. Data Analysis Steps

1. Data Preprocessing
2. Scaling the Data
3. Building the Logistic Regression Model
4. Model Evaluation
5. Model Interpretation
6. Prediction for a New Patient

#### 4. Data Visualization

- Bar Plot: Displays the count of patients with and without heart disease (sns.countplot(x='target', data=df)).

Pair Plot: Shows relationships between selected features (age, trestbps, chol, thalach) and the target using sns.pairplot(). This helps visualize correlations between features and their separability based on the target label.

Heatmap: Visualizes the correlation matrix of all features (sns.heatmap()). This heatmap helps to identify multicollinearity among the features.

Coefficient Bar Plot: Displays the coefficients (or weights) of the logistic regression model for each feature. This plot provides insight into how much each feature influences the prediction.

Confusion Matrix: Displays the confusion matrix (true positives, false positives, true negatives, false negatives) using ConfusionMatrixDisplay().

Precision-Recall Curve: A curve that shows the trade-off between precision and recall for different threshold values of the model's predictions.

ROC Curve: A Receiver Operating Characteristic (ROC) curve showing the model’s ability to discriminate between classes at different threshold levels, along with the Area Under the Curve (AUC) to quantify performance.

#### 5. Key Findings
      
- Thalach (maximum heart rate achieved) is positively correlated with the target (patients with heart disease tend to have lower maximum heart rates).
- Chest pain type (cp) is also strongly correlated with the presence of heart disease.
- Exercise-induced angina (exang) and oldpeak have negative correlations with the target, meaning patients with these conditions are more likely to have heart disease.
- The confusion matrix shows that the model performs fairly well with accuracy of 82% on the test data.
- The model predicts the probability of heart disease for a specific patient, with a detailed output showing both the predicted class and the corresponding probabilities. This is critical for making personalized medical decisions.

#### 6. Source

https://archive.ics.uci.edu/ml/datasets/Heart+Disease
