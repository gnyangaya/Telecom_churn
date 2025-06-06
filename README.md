
# SyriaTel Customer Churn Prediction

## Project Overview

Customer retention is a critical challenge for telecom companies, where pricing is often uniform and competition is intense. This project builds a machine learning classifier to predict customer churn for SyriaTel, a leading telecommunications provider. The goal is to flag customers most at risk of leaving, so that timely and targeted retention actions can be taken.

## Business Context

- **Problem**: SyriaTel currently lacks a reliable, data-driven method for identifying customers likely to churn. This leads to missed opportunities for proactive engagement.
- **Why it matters**: Retaining customers is significantly more cost-effective than acquiring new ones.
- **Objective**: Develop a predictive model that can highlight churn risk using customer-level data, ultimately improving retention efforts.

## Dataset Overview

The dataset included features such as:
- Customer service interactions
- Call usage (day, evening, night, international)
- Number of voicemail messages
- Subscription type
- Churn status (target variable)

Note: The data had a strong class imbalance — far more customers stayed than churned — which influenced model selection and evaluation.

## Modelling Approach

We used a classification approach to predict churn (yes/no). Four models were tested:

1. **Baseline Logistic Regression**: A simple linear model to establish a benchmark.
2. **Balanced Logistic Regression**: Handled class imbalance using built-in weighting.
3. **Decision Tree (Baseline)**: Captured non-linear relationships between features and churn.
4. **Tuned Decision Tree (Final Model)**: Optimised for depth, leaf size, and class weighting to maximise performance.

## Evaluation Strategy

Due to class imbalance, we focused on business-relevant metrics:

- **Recall**: How many churners we correctly identified (priority metric)
- **Precision**: How many flagged churners were correct (to avoid false alarms)
- **AUC Score**: How well the model separates churners from non-churners
- **Train/Test Accuracy**: Used to check for overfitting or underfitting

## Final Model: Tuned Decision Tree

- **Recall (churners)**: 0.83 — successfully identified 83% of actual churners
- **Precision**: 0.79 — low false positives
- **AUC Score**: 0.91 — highest of all models
- **Train/Test Accuracy**: Very close (≈94%) — strong generalisation

## Key Recommendations

- Use the model to flag at-risk customers and prioritise them for retention efforts.
- Focus on actionable and cost-effective interventions for flagged customers.
- Monitor model performance periodically to ensure consistent accuracy.

## Next Steps

- Test the model's effectiveness by applying it to real customer data in a controlled environment.
- Evaluate the business impact of retention actions guided by the model’s predictions.
- Consider revisiting model performance after further customer behaviour data is collected.

## Author

George Nyang’aya
