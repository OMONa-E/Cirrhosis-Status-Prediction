# Cirrhosis Prediction using Mayo Clinic PBC Dataset

This repository contains a comprehensive analysis and predictive model for cirrhosis using the Mayo Clinic primary biliary cirrhosis (PBC) dataset. The analysis aims to predict patient status based on various clinical features.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Preprocessing](#preprocessing)
- [Modeling](#modeling)
- [Feature Importance](#feature-importance)
- [Results](#results)
- [Conclusion](#conclusion)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## Introduction

Cirrhosis is a late stage of scarring (fibrosis) of the liver caused by many forms of liver diseases and conditions, such as hepatitis and chronic alcoholism. This project uses data from the Mayo Clinic trial in primary biliary cirrhosis (PBC) of the liver conducted between 1974 and 1984 to predict patient status.

## Dataset

The dataset contains information on 424 PBC patients, including various clinical measurements and patient outcomes. The dataset is described in detail in the references provided in the acknowledgements.

### Attribute Information

1. **ID**: Unique identifier
2. **N_Days**: Number of days between registration and the earlier of death, transplantation, or study analysis time in July 1986
3. **Status**: Status of the patient (C: censored, CL: censored due to liver transplant, D: death)
4. **Drug**: Type of drug (D-penicillamine or placebo)
5. **Age**: Age in days
6. **Sex**: Gender (M: male, F: female)
7. **Ascites**: Presence of ascites (N: No, Y: Yes)
8. **Hepatomegaly**: Presence of hepatomegaly (N: No, Y: Yes)
9. **Spiders**: Presence of spiders (N: No, Y: Yes)
10. **Edema**: Presence of edema (N: no edema and no diuretic therapy for edema, S: edema present without diuretics, or edema resolved by diuretics, Y: edema despite diuretic therapy)
11. **Bilirubin**: Serum bilirubin in mg/dl
12. **Cholesterol**: Serum cholesterol in mg/dl
13. **Albumin**: Albumin in gm/dl
14. **Copper**: Urine copper in ug/day
15. **Alk_Phos**: Alkaline phosphatase in U/liter
16. **SGOT**: SGOT in U/ml
17. **Triglycerides**: Triglycerides in mg/dl
18. **Platelets**: Platelets per cubic ml/1000
19. **Prothrombin**: Prothrombin time in seconds
20. **Stage**: Histologic stage of disease (1, 2, 3, or 4)

## Installation

To run the analysis, you need to have Python installed along with the following packages:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn
- plotly

You can install the required packages using the following command:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn plotly
```

## Exploratory Data Analysis

The exploratory data analysis (EDA) involves visualizing the distributions of the features, checking for missing values, and understanding the relationships between the features and the target variable (Status).

## Preprocessing

The preprocessing steps include:

- Handling missing values.
- Encoding categorical variables.
- Scaling numerical variables.
- Addressing class imbalance using SMOTE.

## Modeling

Various machine learning models are evaluated to predict the patient status:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- k-Nearest Neighbors

Hyperparameter tuning is performed using GridSearchCV to find the best model.

## Feature Importance

Feature importance is evaluated using the Gradient Boosting classifier and permutation importance. The top features are visualized to understand their impact on the model predictions.

## Results

The Gradient Boosting classifier performs the best among the evaluated models. The most important features for predicting patient status are identified and visualized.

## Conclusion

This analysis provides a comprehensive approach to predicting cirrhosis status using clinical data. The Gradient Boosting classifier, along with feature importance analysis, helps in understanding the critical factors affecting patient outcomes.

## Acknowledgements

The dataset and analysis are based on:

- Fleming, T.R. and Harrington, D.P. (1991) Counting Processes and Survival Analysis. Wiley Series in Probability and Mathematical Statistics: Applied Probability and Statistics, John Wiley and Sons Inc., New York.
- Dickson, et al., Hepatology 10:1-7 (1989)
- Markus, et al., N Eng J of Med 320:1709-13 (1989)

Dataset retrieved from [Kaggle](https://www.kaggle.com/fedesoriano/cirrhosis-prediction-dataset).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
