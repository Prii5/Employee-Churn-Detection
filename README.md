#  HR Analytics Dashboard

This project presents an end-to-end HR analytics solution, combining exploratory data analysis, feature engineering, and  predictive modeling to better understand and anticipate employee attrition.


## Project Overview

Employee attrition is a critical issue that directly impacts organizational performance and costs. This notebook investigates key factors contributing to attrition and builds predictive models to identify employees at risk of leaving the company.


##  Key Objectives

- Explore and visualize key drivers of attrition such as distance from home, job role, and income
- Handle class imbalance to improve model sensitivity to rare attrition cases
- Compare model performance before and after balancing
- Build interpretable and scalable ML pipelines using scikit-learn



## EDA Highlights

- **Commute Distance**: Employees who left the company lived farther from work (avg. 10.4 miles) than those who stayed (avg. 8.9 miles)
- **Role-wise Tenure**: Managerial roles show longer tenure; Sales Reps show the shortest
- **Years at Company vs Income**: Positive linear trend observed



##  Modeling Summary

The project involved training and evaluating two classification models — Random Forest Classifier and Logistic Regression — to predict employee attrition. Both models were tested in two configurations: one with the original (imbalanced) dataset and another after applying class balancing techniques.

1.**Random Forest Classifier**  
  - Initially, the Random Forest model performed well on overall accuracy, achieving 87%. However, it failed to effectively identify employees likely to leave, with a very low recall score of 10% for the "Yes" (attrition) class.  

  - After applying class balancing, the recall for attrition improved to 21%, and the F1-score rose to 30%, while the overall accuracy remained unchanged at 87%. This indicated better sensitivity to attrition without compromising the model’s overall performance.


2.**Logistic Regression**  
  - Without any balancing, Logistic Regression showed strong overall performance with  89% accuracy and managed to capture 44% of attrition cases, making it a relatively balanced choice even without resampling. 

  - After applying balancing techniques, the model became more sensitive to attrition, achieving a  higher recall of 62%. However, this came at the cost of reduced overall accuracy and precision, as it misclassified more non-attrition cases.



##  Tech Stack

- Python, Pandas, NumPy
- Seaborn, Matplotlib for EDA
- scikit-learn for preprocessing and modeling
- Pipelines & ColumnTransformer for workflow automation


