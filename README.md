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


**1)What does the model you have implemented do and when should it be used?**
The implemented model is a Gradient Boosting Machine for regression tasks. It creates a series of decision trees, each aiming to correct the errors of its predecessors. This ensemble approach progressively reduces the overall prediction error.
Use this model when:
You're dealing with structured data and need high predictive accuracy.
Your regression problem involves complex, non-linear relationships between features and the target variable.
You're willing to trade some interpretability for improved predictive performance.
You have sufficient computational resources, as GBM can be demanding.

**2)How did you test your model to determine if it is working reasonably correctly?**
The model's correctness was verified through several steps:
A synthetic dataset was generated to ensure known properties.
The data was split into training and test sets.
The model was trained on the training data and used to predict the test set.
Mean Squared Error (MSE) was calculated to quantify prediction accuracy.
A scatter plot comparing actual vs. predicted values was created, allowing visual assessment of the model's performance.
The plot includes an ideal fit line (y=x) to easily spot deviations in predictions.
This multi-faceted approach combines numerical metrics with visual inspection to comprehensively evaluate the model's performance.

**3)What parameters have you exposed to users of your implementation in order to tune performance?**
The implementation exposes three key parameters:
a) n_estimators: Controls the number of trees in the ensemble. More trees can improve accuracy but increase computation time.
b) learning_rate: Determines how strongly each tree's predictions are weighted. Lower rates can lead to better generalization but may require more trees.
c) max_depth: Limits the depth of individual trees, helping to prevent overfitting.

**4)Are there specific inputs that your implementation has trouble with? Given more time, could you work around these or is it fundamental?**
The current implementation faces challenges with:
High-dimensional data: Performance may degrade with many features.
Categorical variables: These require pre-processing as the model expects numerical inputs.
Large datasets: The model may become slow with very large amounts of data.
Overfitting: Without proper regularization, the model might overfit on small datasets.

Given more time, these limitations could be addressed:
Implement feature importance and selection techniques for high-dimensional data.
Add built-in handling of categorical variables.
Incorporate subsampling methods for better performance on large datasets.
Implement regularization techniques and cross-validation for improved generalization.
