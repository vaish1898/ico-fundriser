**Predicting Success of ICO Fundraiser Campaigns**

**Introduction**

Crowdfunding has gained significant traction as a way for companies to raise funds, and Initial Coin Offerings (ICOs) have emerged as a prominent method for such fundraising, involving the issuance of digital coins. This report explores the prediction of ICO fundraising success using machine learning techniques.

**Objective**

The goal is to predict whether a fundraising project will meet its target or not using a dataset of ICO projects, and identify factors influencing their success.

**Methodology**

The CRISP-DM methodology is employed for this analysis, ensuring a structured approach from data understanding through to deployment.

**Data Understanding**

The dataset contains 2767 records and 16 variables, with a mix of categorical, numeric, and binary variables, such as project success, price of the blockchain coins, team size, and social media presence indicators.

**Data Quality Analysis**

The dataset was analyzed for completeness, accuracy, consistency, and outliers:

Missing values were found in "priceUSD" and "teamSize."

Accuracy and consistency were generally high for most variables.

Outliers were detected using the IQR method and treated using Winsorization.

**Data Preparation**

Missing Data: Median imputation was used for missing values in the "priceUSD" and "teamSize" columns.

Data Cleaning: Duplicate rows were removed, and improper data types were corrected.

Outlier Treatment: Winsorization replaced extreme values in the dataset.

Feature Engineering: Categorical variables were transformed to numerical formats where needed, such as converting the "success" variable to binary (0 and 1).

**Data Transformation**

Normalization: Min-max scaling was applied to numerical variables to ensure consistency across features.

Class Balancing: The dataset was imbalanced, with more "N" (no success) than "Y" (success). Over-sampling was used to balance the target class distribution.

Data Splitting: The dataset was split into an 80:20 ratio for training and testing the models.

**Modelling**

Two models were selected for the analysis:

Random Forest: Chosen for its ability to handle complex relationships and high-dimensional data.

Support Vector Machine (SVM): Effective for high-dimensional spaces and capturing non-linear patterns.

**Model Results**

Random Forest achieved the following performance metrics:

Accuracy: 82.99%

Precision: 85.30%

Recall: 79.70%

F1 Score: 82.41%

Support Vector Machine achieved:

Accuracy: 70.30%

Precision: 71.38%

Recall: 67.76%

F1 Score: 69.53%

**Cross-Validation Results**

Random Forest: Accuracy ranged from 77.31% to 79.88% across different tuning parameters.

SVM: Accuracy ranged from 66.75% to 67.31% based on tuning parameters.

**Conclusion**

The Random Forest model performed better than the Support Vector Machine model, with higher accuracy and more balanced performance across metrics. This makes Random Forest a more reliable model for predicting the success of ICO fundraising campaigns.
