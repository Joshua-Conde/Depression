# Depression

## Overview

This README provides detailed information about the dataset, the target variable, and the performance of the final linear regression model.

## Dataset Description

The dataset consists of data collected from individuals participating in a study related to mental health conditions. It includes various features such as activity levels, demographic information (age, gender, education), clinical parameters, and scores related to depression assessment.

### Features

- **Activity**: Level of physical activity measured using an actigraph device.
- **Days**: Number of days observed or recorded.
- **Gender**: Gender of the participant (categorical: Male, Female).
- **Age**: Age group of the participant.
- **Education (Edu)**: Educational qualification of the participant.
- **Affection Type (Afftype)**: Type of affection or mental health condition.
- **Melancholia (Melanch)**: Indicates presence or absence of melancholia.
- **Inpatient**: Binary indicator of whether the participant has been admitted as an inpatient.
- **Marriage**: Marital status of the participant.
- **Work**: Employment status of the participant.

### Target Variable

The target variable of interest is the **MADRS Score (MADRS1)**, which stands for Montgomery-Åsberg Depression Rating Scale. It is a widely used scale for assessing the severity of depression symptoms in individuals. Higher MADRS scores indicate more severe depressive symptoms.

## Preprocessing

### Data Cleaning

- The dataset underwent basic cleaning steps to handle missing values and inconsistencies.
- Missing values in the 'melanch' column were imputed with 2.0, indicating no melancholia.
- The 'melanch' column contained values of 3.0, which were replaced with 0.0 to maintain consistency.

### Feature Engineering

- Age groups and educational qualifications were one-hot encoded to convert categorical variables into a format suitable for machine learning algorithms.

### Scaling

- Numeric features ('activity' and 'days') were scaled using `StandardScaler` to ensure that all features contribute equally to the model fitting process.

## Model Building and Evaluation

### Linear Regression Model

- A linear regression model was trained using the preprocessed data to predict the MADRS scores.
- The model achieved the following performance metrics:
  - Mean Squared Error (MSE): 1.1465
  - R-squared (R2): 0.9528

### Interpretation

- The high R-squared value indicates that the model explains approximately 95.28% of the variance in the MADRS scores, suggesting a strong relationship between the features and the target variable.
- The low MSE value indicates that the model's predictions are close to the actual MADRS scores on average.

## Conclusion

The linear regression model built using the provided dataset demonstrates strong predictive capabilities for estimating MADRS scores based on various demographic, clinical, and activity-related features. This model can be valuable for assessing depression severity and monitoring individuals' mental health conditions.
