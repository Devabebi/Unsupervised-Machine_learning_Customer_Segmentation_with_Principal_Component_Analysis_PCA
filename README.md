# Unsupervised-Machine_learning_Using_PCA_to_Optimise_Health_Risk_Prediction_from_Biomarker_Data

I built a supervised machine learning model to predict health risk from biomarker data. The baseline model achieved 92% accuracy already promising, but I wanted to push further.

<img width="2560" height="1344" alt="image" src="https://github.com/user-attachments/assets/fd88a0b5-d12a-491f-8c13-7779bba74d16" />

🔒 Disclaimer
All datasets and reports used in this portfolio are entirely fictitious and contain no proprietary, confidential, or sensitive information from any company, institution, or individual. The information presented is dummy data created solely to demonstrate my capability in using Tableau for advanced analytics within the real estate industry.

## Table of Content
- [Business Overview](#business-overview)
- [Problem Statement](#problem-statement)
- [Project Rationale](#project-rationale)
- [Objectives](#objectives)
- [Project Workflow](#project-workflow)
- [Data Exploration and Preprocessing](#data-exploration-and-preprocessing)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Feature Interpretation](#feature-interpretation)
- [Insight & Recommendation](#insight-and-recommendation)


## Business Overview

<img width="1164" height="1688" alt="image" src="https://github.com/user-attachments/assets/25d61dd5-87d2-43d3-bbf7-8cef551401d9" />

Health risk prediction is a critical task in preventive medicine, enabling early intervention and better patient outcomes. 
Consider a healthcare dataset containing detailed biomarker readings from routine medical checkups. 

Each patient’s record includes numerous features like **cholesterol levels, blood pressure readings, glucose levels, and other biochemical indicators**. 
While these biomarkers are valuable for predicting health risks, their high dimensionality can lead to redundant information, multicollinearity, and overfitting in predictive models.


## Problem Statement

<img width="1807" height="1312" alt="image" src="https://github.com/user-attachments/assets/46cad3d9-51b9-42db-813c-f140cd5afa1b" />

HealthWise Analytics aims to assist healthcare providers in predicting patient health risks based on biomarker data. 
The biomarker dataset contains dozens of features, making model training challenging due to dimensionality. The goal is to:

- **Identify the most critical patterns in biomarker data** using PCA.

- **Build a streamlined, high-performance machine learning model** to predict health risks effectively.

- **Improve interpretability** by relating key principal components back to the original biomarkers.


## Project Rationale

In the era of big data, healthcare organizations are increasingly collecting extensive biomarker data to predict health risks. However, the sheer volume of biomarkers can lead to:

- **Overfitting:** Machine learning models may perform well on training data but fail to generalize to unseen data.

- **Computational Inefficiency:** Large datasets increase computational costs and training time.
  
- **Interpretability Issues:** Identifying key contributing factors becomes difficult with numerous features.


## Objectives

<img width="3000" height="403" alt="image" src="https://github.com/user-attachments/assets/197448b3-20dc-49f8-a046-257a535d2d26" />

To demonstrate how Principal Component Analysis (PCA) reduces the dimensionality of biomarker data, simplifies modeling, and improves interpretation, ultimately enhancing the accuracy and efficiency of a health risk prediction model.


## Project Workflow

- **Step 1:** Data Exploration & Preprocessing:
Handle missing values (e.g., imputation or removal). Scale numerical features as necessary Variable distributions, correlations, and outliers.

- **Step 2:** Model Training:
Train and evaluate models with and without PCA.

- **Step 3:** Model Evaluation:
Evaluate the models using various metrics: accuracy, precision, recall, F1-score.

- **Step 4:** Feature Interpretation:
Relate key principal components to original biomarkers to enhance interpretability.

- **Step 5:** Insights & Recommendations:
Provide actionable insights to healthcare providers.


## Exploratory Data Analysis (EDA) and Preprocessing
Before feeding the data into the machine learning model, I did an extensive data preprocessing. This included handling missing values, outliers, duplicates, encoding categorical features, scaling numerical features, and addressing class imbalance using SMOTE. Additionally, feature engineering techniques were applied to extract relevant information from the raw data.

<img width="1382" height="492" alt="Screenshot 2025-10-25 234643" src="https://github.com/user-attachments/assets/5e1ab407-da68-4619-8236-4a953d783bf4" />

<img width="1390" height="437" alt="Screenshot 2025-10-25 234703" src="https://github.com/user-attachments/assets/08b505ce-eb3d-4577-93fd-ecf4ef045e53" />

<img width="1370" height="672" alt="Screenshot 2025-10-25 234740" src="https://github.com/user-attachments/assets/50cf338f-3b7f-460b-b4b7-66988bc2eba5" />


## Model Training
I used train test split to train my model and was trained with 80% of the data and used the remaining 20% for testing. I applied random_state=42, stratify=y to ensure my data sample values does not change ireespectively of how many times was rerun.

<img width="1407" height="355" alt="Screenshot 2025-10-25 235203" src="https://github.com/user-attachments/assets/112681fb-6cc7-44a6-925b-ddf120e36829" />


## Model Evaluation

<img width="1399" height="638" alt="Screenshot 2025-10-25 234831" src="https://github.com/user-attachments/assets/8f0e34a1-daf8-441b-85bd-2462d026629e" />

<img width="1402" height="669" alt="Screenshot 2025-10-25 234915" src="https://github.com/user-attachments/assets/52dcc319-eb4e-45cf-8861-100a53ed477b" />


## Feature Interpretation

Visualizing feature contributions with and without PCA provides insights into the model's decision-making process and highlights the differences between the original and PCA-transformed features.

- **Without PCA: Feature Importance for Logistic Regression**
For logistic regression, feature importance can be interpreted using the absolute values of the coefficients.

<img width="1400" height="677" alt="Screenshot 2025-10-25 235825" src="https://github.com/user-attachments/assets/821f0a61-70b3-4215-96be-1137976d0584" />

<img width="1355" height="639" alt="Screenshot 2025-10-25 235850" src="https://github.com/user-attachments/assets/cf127d51-f726-4283-a66d-246b30cd7b01" />

- **With PCA: Logistic Regression on Principal Components**
When using PCA-transformed data, visualize how the model interprets the principal components.

<img width="1395" height="463" alt="Screenshot 2025-10-25 235908" src="https://github.com/user-attachments/assets/a243135c-7a2e-4f65-9e53-bbf59e53f370" />

<img width="1220" height="654" alt="Screenshot 2025-10-25 235926" src="https://github.com/user-attachments/assets/defc54c7-793a-43c3-85fd-7b2c36bdd88c" />


## Insight & Recommendation

<img width="1132" height="679" alt="Screenshot 2025-10-26 000534" src="https://github.com/user-attachments/assets/a49e5633-7a74-426c-9095-caa5ca821935" />

- **Without PCA:**
The coefficients directly show the impact of each feature on the target variable.
Positive coefficients indicate an increase in the likelihood of the positive class, while negative coefficients indicate a decrease.

- **With PCA:**
The coefficients of the principal components describe their contribution to the model.
The heatmap helps relate these components back to the original features, enabling interpretation in the original feature space.


## Thank You
Reach out for more info!
<img width="1584" height="396" alt="Python SQL R MachineLearning MySQL DataAnalysis DataVisualization Statistics BigDataAnalysis Pandas NumPy CloudComputing AWS Azure Tableau CommunicationSkills ProblemSolving BusinessIntelligence PostgreSQL" src="https://github.com/user-attachments/assets/79c27f62-8f8d-45ad-8806-8375605448fa" />
