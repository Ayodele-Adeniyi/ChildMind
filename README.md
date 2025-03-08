# Table of Contents

\tableofcontents  
\newpage

## Introduction

This project investigates internet addiction in children and adolescents by predicting scores from the Parent-Child Internet Addiction Test (PCIAT). It evaluates the effectiveness of two machine learning models—**Elastic Net Regression** and **Random Forest**—in estimating PCIAT scores. The dataset used comes from the **Healthy Brain Network (HBN)** and includes various demographic and behavioral features related to internet usage.

The objective is to determine which model provides the best predictive accuracy for estimating PCIAT scores, offering insights into internet usage behaviors among children.

## Dataset

**Source:** [Kaggle - Child Mind Institute: Problematic Internet Use](https://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use/data)

### Features Included

-   **Age** (in years)\
-   **Gender** (Male/Female)\
-   **Weight** (in pounds)\
-   **Body Mass Index (BMI)**\
-   **Sleep Disturbance Scores**\
-   **Hours of Internet/Computer Use**\
-   **PCIAT Scores** (Target Variable)

## Data Preprocessing

Before model training, extensive preprocessing was performed, including:

1.  **Handling Missing Values**:
    -   Missing data was imputed using **Multivariate Imputation by Chained Equations (MICE)** to retain as much information as possible.
2.  **Feature Selection & Exclusion**:
    -   Features with high missing values or low predictive relevance were removed.\
    -   Highly correlated features were excluded to reduce multicollinearity.
3.  **Exploratory Data Analysis (EDA)**:
    -   Scatter plots, histograms, and correlation heatmaps were used to analyze relationships between features and PCIAT scores.

## Methodology

### 1. Model Selection & Implementation

#### **Elastic Net Regression**

Elastic Net is a combination of **Ridge (L2) and Lasso (L1) regression**, helping with both feature selection and regularization. It is particularly useful in handling multicollinearity in datasets.

#### **Random Forest**

Random Forest is an ensemble learning technique that builds multiple decision trees and averages their predictions. It is highly effective for capturing non-linear relationships in the data.

### 2. Evaluation Metrics

To compare model performance, the following metrics were used:

-   **Root Mean Squared Error (RMSE):** Measures prediction error magnitude.\
-   **Scatter Plots:** Visual comparison of actual vs. predicted PCIAT scores.

## Results

The predictive performance of the two models is summarized below:

| Model         | RMSE |
|---------------|-----:|
| Elastic Net   | 16.4420229 |
| Random Forest | 16.9315969 |

The model with the **lower RMSE** is recommended for PCIAT score prediction.
