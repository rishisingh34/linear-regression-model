# Linear Regression README

## Overview
This Python script implements a simple linear regression model using gradient descent for training. The code consists of several functions that handle forward and backward propagation, cost computation, parameter updates, training, and prediction. This README aims to provide an understanding of each function and the overall structure of the script.

## Installation and Usage

### Clone the Repository
You can clone the repository from [https://github.com/rishisingh34/linear-regression-model.git](https://github.com/rishisingh34/linear-regression-model.git) using the following command:

```bash
git clone https://github.com/rishisingh34/linear-regression-model.git
```

### Install Dependencies
Before running the script, make sure to install the required libraries by executing the following command:

```bash
pip install pandas numpy matplotlib
```

### Running the Script
1. Navigate to the cloned repository's directory:

```bash
cd linear-regression-model
```

2. Open the script in your preferred Python environment.

3. Execute the script.

## Libraries
- `pandas`: Data manipulation library
- `numpy`: Numerical operations library
- `matplotlib.pyplot`: Plotting library for data visualization

## Loading Data
The script starts by loading a CSV file named 'data_for_lr.csv' into a Pandas DataFrame (`df`). It then performs data cleaning by removing rows with missing values.

## Splitting Data
The dataset is split into training and validation sets. The first 500 rows are used for training (`train_input` and `train_output`), while the next 199 rows are used for validation (`test_input` and `test_output`).

## Linear Regression Formulas
### Forward Propagation
- Hypothesis: \( f(x) = mx + c \)
- Predictions are calculated using the hypothesis function.

### Cost Function
- Cost function: \( J = \frac{1}{2n} \sum_{i=1}^{n} (y_i - f(x_i))^2 \)
- Measures the difference between predicted and actual values.

### Backward Propagation
- Derivatives are computed for updating parameters.
- \( df = f(x) - y \)
- \( dm = \frac{\sum{df \cdot x}}{n} \)
- \( dc = \frac{\sum{df}}{n} \)

### Update Parameters
- \( m' = m - (\text{learning\_rate} \cdot dm) \)
- \( c' = c - (\text{learning\_rate} \cdot dc) \)

## Model Training
The training function (`train`) iterates through a specified number of iterations, performing forward and backward propagation, updating parameters, and plotting the training process.

## Training
- Initializes parameters with random values.
- Plots the original and predicted values during each iteration.
- Prints and plots the loss over iterations.

## Prediction
- Uses the trained parameters to make predictions on the validation set.
- Plots the predicted values against the actual values.

## Cost of Prediction
- Computes the cost function for the validation set predictions.
