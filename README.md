# KL/SELANGOR RENTAL PREDICTION USING LOGISTIC REGRESSION AND TREES MODELS
**Purpose**

This project is for study only. Caution must be taken as the information/technique used in this project may not be accurate or done in the right way. Also, credits to all the people for the sources used in this project. 

**Problem statement**

When it comes to setting up a rental price or giving out indications, homeowners, valuers, or realtors, tend to rely on the internet to check the rental market rate from property websites such as PropertyGuru, mudah.my, iProperty, and many others. As easy as it may sound, “the inconsistency of information can easily be found in websites as most of the residential property providers did not own its property data. The objective of most residential property web is more focused on providing a platform for users to share their information. Thus, inconsistent information occurs due to different sets of data may not be entered by the same person (Kee Li Yap, 2020). One can choose their preferred rate suitable for their home from the property websites, but how can one assured on the accuracy of the price per the property’s features? Under-pricing can result in a loss of income, while on the other hand, overpricing can make it difficult to rent the property and lose out on a suitable customer base. It is, therefore, crucial to examine the rental price carefully and suggest a fair rental rate that reflects the property’s value (Dong Xue Ying, 2023).

This project will adopt Classification model, hence, we will focus on the rental category instead of a price. 

**Dataset**

In this project, I will use a high-rise housing dataset obtained from Kaggel. (https://www.kaggle.com/datasets/ariewijaya/rent-pricing-kuala-lumpur-malaysia). This project utilises Jupyter Notebook Python for the entire modeling process.

**Algorithms and Metrics**

Commonly used models for predicting housing rental include Logistic Regression, Decision Trees, Random Forests, and Gradient Boosting algorithms. The evaluation of all models will be using the Confusion Matrix, Classification Report, F1 score, Matthews Correlation Coefficient, and ROC AUC.
The models will be trained in 3 ways, by default, with parameter and with GridSearchCV. The model with the highest score will be selected as the best model for prediction.

**Findings**

1. Dataset Overview and Imbalance
The target variable, rent_category, is highly imbalanced with the distribution:
Low: 12,999, Medium: 6,902, High: 90
This severe imbalance poses a significant challenge for model training and evaluation.

2. Model Performance
Multiple models were trained including Logistic Regression, Decision Tree, Random Forest, and Gradient Boosting.
Performance metrics such as F1 score, Matthews Correlation Coefficient, and ROC AUC were evaluated for each model.
Gradient Boosting with parameter is selected as the best model for now.

3. Effect of Data Imbalance
The imbalance in the dataset heavily influences the model performance, leading to potential biases toward the majority class (Low rent category).
Metrics like ROC AUC and Matthews Correlation Coefficient indicate that while some models perform well, the imbalance needs to be addressed to improve predictions for minority classes.

**Risk/Assumption/Limitation**

Model Bias: Machine learning models can be biased towards the majority class during training. In this case, a model trained on this data might perform well for "low" rentals but perform poorly for "medium" and "high" rentals due to a lack of sufficient data for these categories. This can lead to inaccurate predictions and unreliable risk assessments for these rental categories.

Class Imbalance: The extreme imbalance between "low" and other categories suggests potential class imbalance issues. Techniques like oversampling, undersampling, or cost-sensitive learning might be necessary to address this imbalance and improve model performance for minority classes in the future.

Rental Market Representation: The data is assumed to be representative of the actual rental market distribution. If the data comes from a specific source or region with a unique rental landscape, it might not generalize well to other markets.
Limited Generalizability: The model might not perform well on unseen data with a different rental category distribution. For example, if the model is deployed in a market with a higher proportion of "medium" or "high" rentals, its predictions might be unreliable.

Data Quality: Data quality can affect the model's performance. Errors, missing info, or inconsistencies in the data can lead to unreliable model predictions.

Data Understanding: Building a good model requires a deep understanding of the data and its industry. Failing to grasp the data and its context can lead to flawed models. Data analysis is essential for translating raw data into insights that guide effective model building.
