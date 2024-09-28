# 📊 Bias & Variance Analysis

This project is inspired by the *Introduction to Machine Learning* textbook by Alpaydin. The purpose of this project is to deepen the understanding of the bias-variance tradeoff in regression models by simulating data, fitting polynomial models, and calculating bias and variance errors.

## ⚙️ Problem Overview

We aim to investigate how polynomial regression models of varying complexity perform on a noisy dataset. The ground truth function used is:

$$ f(x) = 2 \cos(x) + \tan(0.5x) $$

Gaussian white noise is added to simulate real-world data, and polynomial models of degree 1, 3, and 5 are fitted to this data. The project is divided into two main sections:

1. **Visualizing Polynomial Fits**: 
    - Fit polynomial models to the noisy dataset.
    - Visualize how well models of different degrees fit the data.
2. **Bias-Variance Tradeoff**: 
    - Calculate and plot the bias, variance, and total error for models of increasing complexity.
    - Evaluate the error at 10 equally spaced points between -2 and 3.

### Results and Plots
We generate the following plots:
- **Ground Truth and Noisy Data**: Visualizes the ground truth function along with one noisy dataset.
- **Polynomial Fits**: Shows fits for polynomial degrees 1, 3, and 5, each overlaid with the average fit.
- **Bias-Variance Tradeoff**: Plots total error, bias error, and variance error as a function of model complexity.

## 🛠️ Libraries Used

- `numpy` and `pandas` for data manipulation.
- `matplotlib` for plotting.
- `sklearn.preprocessing.PolynomialFeatures` and `sklearn.linear_model.LinearRegression` for polynomial regression.

### Code Structure
- **Dataset Generation**: Generates 100 noisy datasets based on the ground truth function.
- **Polynomial Regression Models**: Fits polynomial models of varying degrees (1, 3, and 5).
- **Bias-Variance Calculation**: Computes bias, variance, and total errors across different polynomial degrees.
- **Plotting Functions**: Visualizes the regression models and errors.

## 📝 Results

The analysis reveals that as the model complexity increases:
- **Bias Error** decreases (simpler models underfit the data).
- **Variance Error** increases (complex models overfit to noise).
- **Total Error** initially decreases but then increases due to overfitting in complex models.
