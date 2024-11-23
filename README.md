# Project 2

Select one of the following two options:

**TEAM MEMBERS**
Roshan Krishnamoorthy A20592056
Nisha Mayilraj A20592055
Nithish Kannan Kuppal Thulasiraman A20593857

## Boosting Trees

Implement the gradient-boosting tree algorithm (with the usual fit-predict interface) as described in Sections 10.9-10.10 of Elements of Statistical Learning (2nd Edition). Answer the questions below as you did for Project 1.

Put your README below. Answer the following questions.

Steps to use this code to test any dataset:

1)Prepare your dataset:
Ensure your data is in a numpy array format.
For regression, your target variable should be continuous.
For classification, your target variable should be binary (0 or 1).

2)Import the necessary functions:
from your_file_name import GradientBoostingMachine, evaluate_model

3)Load your dataset:
X, y = your_data_loading_function()

4)Call the evaluate_model function:
evaluate_model(X, y, task='regression', n_estimators=100, learning_rate=0.1, max_depth=3)

5)for classification point of view
evaluate_model(X, y, task='classification', n_estimators=100, learning_rate=0.1, max_depth=3)


6)Adjust parameters as needed:
You can modify n_estimators, learning_rate, and max_depth to tune the model.
Change test_size if you want a different train-test split ratio.

7)Interpret the results:
For regression, a lower Mean Squared Error indicates better performance.
For classification, a higher Accuracy indicates better performance.

8)Limitations and Potential Improvements
Current limitations include:
Lack of support for categorical variables
Potential memory issues with very large datasets
No built-in feature importance calculation
Given more time, improvements could include:
Implementing feature importance
Adding early stopping to prevent overfitting
Incorporating more advanced tree-building algorithms
Adding support for classification tasks

9)The gradient boosting tree algorithm is an ensemble method that combines multiple weak learners (decision trees) to create a strong predictive model. It's particularly effective for:
Regression and classification tasks
Handling non-linear relationships in data
Dealing with complex interactions between features
It should be used when high predictive accuracy is needed, especially for structured, tabular data.

