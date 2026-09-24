# Homework 2 — DSCI 552

## 1. Combined Cycle Power Plant Data Set

The dataset contains data points collected from a Combined Cycle Power Plant over six years (2006–2011), when the power plant was operating at full load. The features consist of the following hourly average ambient variables:

- Temperature (`T`)
- Ambient Pressure (`AP`)
- Relative Humidity (`RH`)
- Exhaust Vacuum (`V`)

These variables are used to predict the net hourly electrical energy output (`EP`) of the plant.

### (a) Download the Data

Download the [Combined Cycle Power Plant dataset](https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant).

> **Note:** There are five sheets in the dataset. They are shuffled versions of the same data. Use **Sheet 1**.

### (b) Explore the Data

#### i. Dataset dimensions

How many rows and columns are in the dataset? What do the rows and columns represent?

#### ii. Pairwise scatterplots

Create pairwise scatterplots of all variables in the dataset, including the predictors (independent variables) and the dependent variable. Describe your findings.

#### iii. Summary statistics

Calculate the following statistics for each variable:

- Mean
- Median
- Range
- First quartile
- Third quartile
- Interquartile range

Summarize the results in a table.

### (c) Simple Linear Regression

For each predictor, fit a simple linear regression model to predict the response.

- Describe your results.
- In which models is there a statistically significant association between the predictor and the response?
- Create plots to support your conclusions.
- Are there any outliers that you would like to remove for each of these regression tasks?

### (d) Multiple Linear Regression

Fit a multiple linear regression model to predict the response using all predictors.

- Describe your results.
- For which predictors can you reject the null hypothesis

$$
H_0:\beta_j=0?
$$

### (e) Compare Simple and Multiple Regression Coefficients

Compare your results from part **(c)** with your results from part **(d)**.

Create a plot with:

- The simple linear regression coefficients from part **(c)** on the x-axis
- The multiple linear regression coefficients from part **(d)** on the y-axis

Each predictor should be displayed as one point. Its simple linear regression coefficient should determine its x-coordinate, and its multiple linear regression coefficient should determine its y-coordinate.

### (f) Nonlinear Associations

Determine whether there is evidence of a nonlinear association between any predictor and the response.

For each predictor \(X\), fit a model of the form:

$$
Y=\beta_0+\beta_1X+\beta_2X^2+\beta_3X^3+\epsilon
$$

See the scikit-learn documentation for [generating polynomial features](https://scikit-learn.org/stable/modules/preprocessing.html#generating-polynomial-features).

### (g) Predictor Interactions

Determine whether there is evidence that interactions between predictors are associated with the response.

Fit a full linear regression model containing all pairwise interaction terms. State whether any interaction terms are statistically significant.

### (h) Model Improvement

Determine whether you can improve your model using interaction terms or nonlinear associations between the predictors and the response.

1. Randomly divide the data into:
   - 70% training data
   - 30% testing data
2. Fit a regression model using all predictors.
3. Fit another regression model containing:
   - All possible pairwise interaction terms
   - Quadratic nonlinear terms
4. Remove insignificant variables using their p-values. Be careful when removing variables involved in interaction terms.
5. Evaluate both models on the testing data.
6. Report the training and testing mean squared errors (MSEs) for both models.

### (i) K-Nearest Neighbors Regression

Perform K-nearest neighbors regression using:

- Raw features
- Normalized features

For each approach:

1. Consider

$$
k\in\{1,2,\ldots,100\}.
$$

2. Find the value of \(k\) that gives the best fit.
3. Plot the training and testing errors as functions of \(1/k\).

### (j) Model Comparison

Compare the KNN regression results with the linear regression model that has the smallest testing error. Provide an analysis of the results.

## 2. ISLR: 2.4.1

## 3. ISLR: 2.4.7