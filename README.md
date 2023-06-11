# Linear_Regression
The provided code demonstrates the use of linear regression to predict the impact of years of experience on salary. Linear regression is a statistical modeling technique used to establish a relationship between a dependent variable and one or more independent variables. It assumes a linear relationship between the input variables and the target variable.

Here is a step-by-step explanation of the code:

1. Import necessary libraries: The code begins by importing the required libraries. `LinearRegression` from `sklearn.linear_model` is used for linear regression, and `mean_squared_error` from `sklearn.metrics` is used to evaluate the model's performance. `numpy` is imported as `np` to work with arrays efficiently, and `matplotlib.pyplot` is imported as `plt` for visualization.

2. Define the data: The code defines two arrays, `experience` and `salary`, which represent the years of experience and corresponding salaries, respectively. These arrays hold the data points for training the linear regression model.

3. Reshape the data: The `experience` array is reshaped using `.reshape(-1,1)`. This is necessary because `LinearRegression` expects a 2D array as input, and reshaping with `-1` automatically determines the number of rows based on the size of the input array and ensures that the array has only one column.

4. Create an instance of Linear Regression: The code creates an instance of the LinearRegression model using `LinearRegression()`. This instance will be used to train the linear regression model.

5. Fit the model: The `fit` method is used to train the linear regression model. It takes the `experience` array as the input features and the `salary` array as the target variable. The model adjusts its coefficients to fit the training data.

6. Make predictions: The code uses the `predict` method to make predictions on the `experience` array using the trained linear regression model. The predicted salaries are stored in `salary_pred`.

7. Calculate Mean Squared Error (MSE): The code calculates the mean squared error between the actual salaries (`salary`) and the predicted salaries (`salary_pred`) using the `mean_squared_error` function from `sklearn.metrics`. The resulting MSE is stored in `Mse`.

8. Print model coefficients and intercept: The code prints the coefficient and intercept of the linear regression model using `model.coef_` and `model.intercept_`, respectively. The coefficient represents the impact of experience on salary, and the intercept represents the expected salary when experience is zero.

9. Plot the data and regression line: The code uses `plt.scatter` to create a scatter plot of the actual data points (`experience` and `salary`) and `plt.plot` to visualize the regression line generated by the linear regression model. The plot shows how the predicted salaries (`salary_pred`) align with the actual data points.

10. Customize the plot: The code sets the x-axis label as "experience" and the y-axis label as "salary" using `plt.xlabel` and `plt.ylabel`, respectively.

11. Display the plot: The code displays the plot using `plt.show()`.

In summary, this code performs linear regression on the given data to predict the impact of years of experience on salary. It trains a linear regression model, makes predictions, evaluates the model's performance using mean squared error, and visualizes the results.
