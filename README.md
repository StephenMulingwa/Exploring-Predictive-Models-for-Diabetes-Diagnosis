# Exploring-Predictive-Models-for-Diabetes-Diagnosis

## Introduction
Diabetes is a chronic health condition characterized by elevated blood glucose levels, which can lead to serious health complications such as heart disease, kidney damage, and vision problems if left unmanaged. Early detection and effective diabetes prediction can help in timely intervention and better management strategies. This project leverages a dataset of 253,680 survey responses from the CDC's BRFSS2015 to predict diabetes status based on 21 health indicators. Using machine learning techniques, four models, Logistic Regression, Decision Tree, Random Forest, and XGBoost, were built and evaluated to predict whether one has prediabetes/diabetes or not. The aim is to develop an accurate, interpretable model to assist in healthcare decision-making and risk assessment.

## Notebook Structure
1. Business Understanding
2. Importing Libraries
3. Data Staging
4. Data Understanding
5. Data Preparation
6. Explanatory Data Analysis
7. Data Preprocessing
8. Modelling
9. Model Comparison

## Business Understanding
Diabetes is a growing public health challenge, affecting millions worldwide and posing significant healthcare costs and risks. Identifying individuals at risk of diabetes or prediabetes early can enable preventive measures and improve healthcare outcomes. This project aims to leverage machine learning techniques to predict diabetes status using health indicators from survey data, providing insights into the most influential factors and enabling informed decision-making. By building and evaluating predictive models, the project seeks to support healthcare providers in identifying high-risk individuals efficiently.

### Project Overview
This project focuses on predicting diabetes and prediabetes using a dataset of health indicators collected from 253,680 survey responses to the CDC's BRFSS2015. The dataset includes 21 features, such as BMI, smoking status, and blood pressure, which are analyzed to determine their impact on diabetes risk. The project employs machine learning models—Logistic Regression, Decision Tree, Random Forest, and XGBoost—to classify individuals as diabetic or non-diabetic. By leveraging these models, the project aims to develop a robust predictive tool that can aid in early detection and healthcare decision-making, ultimately contributing to better prevention and management strategies for diabetes.

### Problem Statement
Diabetes is a leading cause of morbidity and mortality worldwide, with its prevalence rising at an alarming rate. Early detection of diabetes or prediabetes is critical for effective management and prevention of complications, yet traditional screening methods can be resource-intensive and inaccessible to some populations. This project addresses the need for a cost-effective, data-driven solution by leveraging machine learning to predict diabetes risk based on easily obtainable health indicators. By developing accurate and interpretable predictive models, this work aims to support healthcare providers in identifying at-risk individuals and prioritizing preventive care.

### Objectives
1. To develop machine learning models that accurately predict diabetes or prediabetes based on health indicators.
2. To identify the most significant factors contributing to diabetes risk.
3. To evaluate and compare the performance of Logistic Regression, Decision Tree, Random Forest, and XGBoost models.
4. To address the class imbalance in the dataset and its impact on predictive accuracy.
5. To create a predictive tool that can be integrated into healthcare workflows for early detection and intervention.

### Research Questions
1. What are the most significant health indicators associated with diabetes risk?
2. How accurately can machine learning models classify individuals with and without diabetes?
3. Which machine learning model performs best in terms of predictive accuracy and reliability?
4. How does class imbalance in the dataset affect model performance, and what strategies can mitigate this?
5. How can the predictive model be integrated into real-world healthcare applications for early diabetes detection?

## Data Understanding
The dataset used in this project, sourced from the CDC's BRFSS2015, consists of 253,680 survey responses with 21 health indicators and one target variable, Diabetes_binary. This binary target variable classifies individuals as either non-diabetic (0) or diabetic/prediabetic (1). The features include demographic, behavioral, and health-related factors such as BMI, smoking status, blood pressure, physical activity, and cholesterol check status. While the dataset is clean with no missing values, it is imbalanced, with fewer diabetic/prediabetic cases compared to non-diabetic cases. Understanding the distribution and relationships among these features is essential for identifying patterns, addressing class imbalance, and optimizing the predictive models.

## Data Analysis
In the data analysis phase, exploratory data analysis (EDA) was conducted to understand the dataset's structure, relationships, and distributions. Most of the features are categorical, and there is a low to moderate correlation between the independent variables, minimizing multicollinearity and enhancing the uniqueness of each feature in predicting diabetes. The histogram analysis revealed that continuous variables, such as BMI, are not normally distributed, with BMI skewed to the right and most values ranging between 20 and 40. A significant class imbalance in the target variable (Diabetes_binary) was observed, with the majority of respondents not having diabetes, necessitating data balancing techniques during model training. I builyte four machine learning models Logistic Regression, Decision Tree, Random Forest, and XGBoost, fine-tuned, and evaluated. All models achieved over 80% accuracy and F1 scores for both training and test datasets, with the Random Forest model performing the best, attaining a test accuracy of 86.57% and an AUC of 0.92, demonstrating its robustness for predicting diabetes.

## Data Visualizations
### Distribution of Diabetes Status

![image](https://github.com/user-attachments/assets/8fae8b4f-169e-4ed2-b214-f12111a039e1)

There is a data imbalance in the outcome variable with the majority of the people not having diabetes. Thus, data balancing will be necessary when building my model.

### Distribution of BMI

![image](https://github.com/user-attachments/assets/4dbc0743-5d9c-470e-b970-7272bd586d0d)

The histogram above shows that the population's BMI is skewed to the right. With a majority of the people having a BMI of between 20 and 40.

### High Blood Pressure Vs Diabetes

![image](https://github.com/user-attachments/assets/6f73cd01-ec15-4136-923c-d7309aee374b)

Based on the barplot people with High blood pressure are at higher risk of developing Diabetes.

### Model Perfomance comparison

![image](https://github.com/user-attachments/assets/9f29d76a-e0b3-4b06-a015-38ea998de927)

Across the 4 models I built, all has high accuracy in both the training and the test accuracy. Notebly, Random Forest had the highest achieving training accuracyof 88.86% and test accuracy of 86.57%

![image](https://github.com/user-attachments/assets/849a917b-54cb-4d14-92e1-d211c6f8b23a)

All the models have high area uner the curve of over 0.88. Random Forest is the best performing model since it has the highest area under the curve of 0.92

## Conclusion
This project successfully utilized machine learning models—Logistic Regression, Decision Tree, Random Forest, and XGBoost—to predict diabetes risk based on 21 health indicators from the CDC's BRFSS2015 dataset. Through exploratory data analysis, we identified key factors influencing diabetes risk, including BMI, blood pressure, and mental health. The Random Forest model emerged as the best performer, with a test accuracy of 86.57% and an AUC of 0.92, highlighting its robustness in predicting diabetes. Significant predictors identified by the Random Forest model include difficulty in walking/climbing, mental health, general health, income, and BMI. These insights offer valuable guidance for healthcare providers in identifying at-risk individuals and developing targeted interventions. The findings demonstrate the potential of machine learning in enhancing early detection and management of diabetes, supporting the implementation of cost-effective and timely preventive care strategies.

## Recommendations
1. Target High-Risk Groups: Based on the significant predictors identified in the Random Forest model, healthcare providers should prioritize individuals reporting difficulty in walking or climbing, poor mental health, and lower general health. These factors are strong indicators of increased diabetes risk and should be monitored closely for early intervention.
2. Income-Based Healthcare Access: Since income was a significant predictor, it’s essential to ensure that lower-income individuals have access to diabetes prevention programs, as they might be at higher risk due to limited access to healthcare, nutrition, and lifestyle interventions. Tailoring programs for these populations could improve prevention efforts.
3. Promote Healthy Lifestyle Interventions: Given that BMI was a significant predictor, health campaigns should focus on promoting weight management, physical activity, and healthy eating to reduce obesity and its associated risk factors. Interventions aimed at improving physical mobility could also be valuable in preventing diabetes.
4. Mental Health and Diabetes Prevention: The connection between mental health and diabetes risk highlights the importance of addressing mental health issues such as stress, depression, and anxiety. Healthcare systems should consider integrating mental health support into diabetes prevention programs, recognizing the role mental well-being plays in overall health.
5. Expand Screening for At-Risk Groups: To better predict and prevent diabetes, healthcare systems should consider expanding screening efforts for individuals who report difficulty in walking, poor mental health, or low general health. These screenings can be part of routine check-ups to catch at-risk individuals early.
6. Refine Targeted Interventions Based on Income: Health policies should address the needs of lower-income populations by providing subsidized programs for diabetes prevention, including access to affordable physical activity resources, nutrition education, and regular health check-ups.
7. Continuous Model Evaluation and Updates: As more data becomes available, continually updating the model to reflect changes in predictors like general health or mental health trends will ensure the prediction tool remains accurate and relevant, supporting long-term diabetes prevention efforts.

## References

Slides Presentation Link: [Presentation.pdf](https://docs.google.com/presentation/d/1s5lnwSJkWpb4cHHrOUHFC6TZIw2_saXklP4ubmOoMFo/edit#slide=id.g31cb485869b_0_1)
