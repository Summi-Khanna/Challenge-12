# Credit Risk Analysis

## Overview of the Analysis
    Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans.In this analysis, I  am using various techniques to train and evaluate models with imbalanced classes.

### The purpose of the analysis:
    The purpose of this analysis is to determine if the assessment of the creditworthiness of borrowers on peer-to-peer lending platforms can be automated  using a classification model
### Dataset used and prediction variables:
    Used dataset of historical lending activity from a peer-to-peer lending services company with the following input features:
      - loan_size
      - interest_rate
      - borrower_income	
      - debt_to_income	
      - num_of_accounts	
      - derogatory_marks
      - total_debt
      
    The output is `loan_status` column where 0 represents Healthy loans and 1 represents high risk loans


### Stages of Machine Learning:
1. Data Collection & data processing: using the dataset and splitting it as training set and testing set
2. Choosing a model- Logistic Regression: To categorize the riskiness of the loans as `high risk` and `healthy loans`,`logistic regression`is selected as        model
3. Training data: using the model, fitting the trained data
4. Prediction: using trained model to predict values for testing data
5. Evaluation: evaluating model's performance by doing the following:
      - Calculate the accuracy score of the model
      - Generate a confusion matrix
      - Generate classification report
6. Resampling Training Data: Oversampling the traning data as it is imbalanced data, by using `RandomOverSampler`
7. Train, Test & Evaluate the model with Resampled data: after this evaluation metrics is generated for `LogisticRegression` model
 

## Technologies

It supports Python 3.7 and above and has been constructed in the jupyter lab notebook named ```forecasting_net_prophet.ipynb```
Additionally, the following packages/libraries are used to run the analysis:

- [pandas](https://pypi.org/project/pandas/) - for analyzing data
- [jupyter](https://pypi.org/project/jupyter/) - for an IDE
- [hvplot](https://pypi.org/project/hvplot/) - for creating interactive Visualizations of data
- [holoviews](https://pypi.org/project/holoviews/) - for creating interactive plots
- [colab]() - For running a jupyter server remotely
- [numpy]() - For numerical operations
- [pystan]() - For statistical modeling and high-performance statistical computation
- [fbprophet]() -For forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects.

---

## Installation Guide

Before running the application first install the following dependencies:

```python
  pip install pystan
  pip install fbprophet
  pip install pandas 
  pip install hvplot
  pip install holoviews

```

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
