# Theory of prediction

This repository contains work completed in the university course "Theory of prediction". The course is divided into two blocks: regression analysis, time series.

## Significance of factor and confidence intervals

This file implements the Fisher test and the Student t test. In addition, 95% confidence intervals were calculated for the model coefficients and confidence intervals were constructed for the prediction and for the response.

<div align="center">
  <img src="https://github.com/user-attachments/assets/d1ad502b-8c56-4f02-b678-496244918dc5">
</div>

<div align="center">
  <i>Regression line and confidence intervals</i> 
</div>
 


## Study of residues

Implementation of checking the adequacy of the model. The adequacy of the model is checked using:

1. checking the constancy of the mathematical expectation
   * plot of residues
   * variance analysis of errors through residuals
2. checks for consistency of variance
   * plot of residues
   * White's criterion
   * Goldfeld-Quandt test
3. checking for absence of autocorrelation
   * autocorrelation function graph
   * Ljung-Box Q test
4. checking agreement with normal distribution
   * histogram + density plot
   * probability paper
   * Pearson-Fisher chi-square-test
  
## Trend, seasonality, ACF

This .ipynb file processes two datasets: one with a trend, the other with seasonality. The purpose of processing both datasets was to reduce the time series to a stationary form and subsequently test stationarity using the Dickey-Fuller test.


The series with a pronounced trend was reduced to stationary using the least squares method and calculating differences.

A series without a trend is brought to a stationary form using the following methods:

* using the least squares method, estimate the periodic trend in the form of trigonometric sky expansion (a segment of the Fourier series)
* introducing indicators (Boolean variables) for each time of day (0 hours, 2 hours, ..., 24 hours) and estimation of coefficients using the least squares method
* calculating the periodic trend as an average for each hour
* calculation of periodic differences

## Autoregressive model

A number of actions were performed:

* determining whether this series will be stationary
* definition the recurrence formula for the autocorrelation function (ACF)
* definition of analytical expression for ACF
* creating sample ACF and PACF plots
* using the least squares method, the coefficients of the <i>AR(p − 1)</i>, <i>AR(p)</i> and <i>AR(p + 1)</i>
* the residuals of these models were found, their ACFs were constructed and the variances were estimated
* predictions were made for each model
