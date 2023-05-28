# CompSci Project 1 in Machine Learning: 
# Testing up-to-date machine learning techniques for the modelling of meridional heat transport in the Northern Hemisphere.

Inspired by the work of [Stone, 1978](https://www.sciencedirect.com/science/article/pii/0377026578900064), I performed a polynomial fit analysis on the non-dimensional meridional heat transport equation, using a series of machine learning techniques. After applying plain Ordinary Least Squares (OLS) and Ridge regression, as well as their Bootstrap and Cross-Validation resampling variations, I concluded that the polynomial degree should be at least 6, in order to achieve a satisfactory bias-variance trade-off. Moving into choosing the optimal polynomial coefficients, I used plain Gradient Descent (GD) and Stochastic Gradient Descent (SGD), both with and without momentum, on OLS and Ridge regression. The learning rate was tuned by varying its constant values and exponentially but I also tested the effects of Adaptive Gradient Algorithm (AdaGrad), Root Mean Square propagation (RMS-prop) and ADAptive Moment estimation (ADAM) tuning techniques. Using the simplest variation, GD for OLS with a constant learning rate, resulted in a polynomial exceptionally close to the one acquired from the theoretical solution, that is the inversion of the Hessian matrix, for a version of Stone's equation that includes random noise. 

All of the calculations for this project can be found in the folder "Project1". In particular:
* files "0.1.OLS.ipynb"-"93.ADAM SGD-m.ipynb" are the independent codes/runs for each question.
* file "Project_1_code.ipynb" is the entire code. Basically codes 0.1-93 in a single .ipynb file.
* file "_Christina_Kappatou_Project_1_CompSci.pdf" is the final report.
* file "final polynomial.ipynb" is a final run of the theoretical solution and the GD-OLS one, in order to get the pol. coefficients. 
* file "methods_comparison.ods" is a spreadsheet comparing the MSE and running t ime of each method.
* file "overleaf.txt" is the code for writting the report in Overleaf code.

My final report (Christina_Kappatou_Project_1_CompSci.pdf) also lies there.

# CompSci Project 2&3 in Neural Networks and Gaussian Processes:
# Modelling the meridional heat transport at the Top of the Atmosphere, using a Feed Forward Neural Network and Gaussian Process Regression.

In a non-analytical effort to assess the meridional heat transport at the Top of the Atmosphere (TOA), I estimated the training error using a sinusoidal fit, with a Feed Forward Neural Network (FFNN). For the NN,  5 different activation functions were combined with 6 different ways to tune the learning rate for the stochastic gradient descent. With the results leading to fairly large training errors, even for the optimum combination of a sigmoid activation function with a constant learning rate, I moved to approaching the heat flux curve differently, this time employing Gaussian Process regression with 3 different percentages of train/test data. As expected, decreasing the amount of train data points leads to high train errors and large confidence intervals, rendering the approaching of the curve less reliable.

All of the calculations for this project can be found in the folder "Project". In particular:
* int eh folder "heat_transfer_data" I have stored all of the datasets I used from [Earth's radiation budget from 1979 to present derived from satellite observations](https://cds.climate.copernicus.eu/cdsapp#!/dataset/satellite-earth-radiation-budget?tab=overview). These are from 2000-2022. In any future work I will have to seek for all of the available data, beginning from 1979.
* files "2) Neural Networks.ipynb" and "3) Gaussian Process Regression.ipynb" are the independent codes/runs for each part.
* file "Christina_Kappatou_Projects_2&3.pdf" is the final report.
* file "overleaf.txt" is the code for writting the report in Overleaf code.
