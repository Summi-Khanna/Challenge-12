# Credit Risk Analysis


## Overview of the Analysis
Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans.In this analysis, I  am using various techniques to train and evaluate models with imbalanced classes.



### I. The purpose of the analysis:
The purpose of this analysis is to determine if the assessment of the creditworthiness of borrowers on peer-to-peer lending platforms can be automated  using a classification model


### II. Dataset used and prediction variables:
Used dataset of historical lending activity from a peer-to-peer lending services company with the following input features:
      - loan_size
      - interest_rate
      - borrower_income
      - debt_to_income
      - num_of_accounts
      - derogatory_marks
      - total_debt
      
The output is `loan_status` column where 0 represents Healthy loans and 1 represents high risk loans


### III. Stages of Machine Learning:
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


## IV. Results

The models are evaluated using accuracy, precision, and recall. The precision and recall values represent the label of interest

* Machine Learning Model 1: Linear Regression Model with Original training data

  * Accuracy: 0.95 (95%) given by balanced accuracy score, which indicates 95% of the predicted values are correct
  * Precision: For 0 label, the precision is 1 which indicates that the model is very good in identifying healthy loans and all healthy loans are correctly identified under label 0. For 1 label, the precision is 0.85(85%)which indicates that 85% of the values that the model predicted as high-risk are correct
  * Recall: For Label 1, the recall is 0.91(91%) which means of all the actual high risk loans(support value of 1 label is 619) the model rightly labelled 91% of them as high-risk. For label 0, the recall is 0.99 which inndicates that 99% of the values are rightly labelled

![model-1](https://github.com/Summi-Khanna/Challenge-12/blob/main/Images/model-1.png)


* Machine Learning Model 2: Linear Regression Model with Oversampled training data

  * Accuracy: 0.99 (99%) given by balanced accuracy score, which indicates 99% of the predicted values are correct
  * Precision: For 0 label, the precision is 1 which indicates that the model is very good in identifying healthy loans and all healthy loans are correctly identified under label 0. For 1 label, the precision is 0.84(84%)which indicates that 84% of the values that the model predicted as high-risk are correct
  * Recall: For Label 1, the recall is 0.99(99%) which means of all the actual high risk loans(support value of 1 label is 619) the model rightly labelled 99% of them as high-risk. For label 0, the recall is 0.99 which inndicates that 99% of the values are rightly labelled

![model-2](https://github.com/Summi-Khanna/Challenge-12/blob/main/Images/Model-2.png)
  

## V. Summary

Both Logistic Regression models performed quite well. Training the Logistic Regression model with the randomly oversampled dataset increased both accuracy and recall without any sacrifice in precision. there is a slight difference depending on the model trained via the original versus the resampled data. Model 2 has high recall value (0.99) for high-risk loans with precision value of 0.99 as being compared to model 1. The accuracy rate is better in model-2 (99%) as comapred to model-1 (95%) Model-2 is recommended over Model-1. 

---

## Technologies

It supports Python 3.7 and above and has been constructed in the jupyter lab notebook named `credit_risk_resampling.ipynb`
Additionally, the following packages/libraries are used to run the analysis:

- [pandas](https://pypi.org/project/pandas/) - for analyzing data
- [jupyter](https://pypi.org/project/jupyter/) - for an IDE
- [numpy](https://pypi.org/project/numpy/) - For numerical operations
- [sklearn.metrics](https://pypi.org/project/scikit-metrics/)- for importing differnet metrics

---

## Installation Guide

Before running the application first install the following dependencies:

```python
  pip install pandas 
  pip install imbalanced-learn
  pip install pydotplus

```
---

## Usage

To view the analysis, clone the repository using "git clone <link>" and then navigate to the file named `credit_risk_resampling.ipynb` notebook in the [repository directory](https://github.com/Summi-Khanna/Challenge-12)

--- 

## Contributors
 
Summi Khanna  
Email : sam.summo2812@gmail.com <br>
LinkedIn : https://www.linkedin.com/in/summi-khanna-004a60187/

---

## License

MIT License

Copyright (c) 2021 Summi Khanna

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---
