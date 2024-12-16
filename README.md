# Lung Cancer Prediction Using Cigarette Consumption and Pollution Data

## Introduction

Lung cancer is the leading cause of death among all cancers, which is why we undertook this project to explore its relationship with cigarette consumption and air pollution.

We aim to predict lung cancer mortality rates based on over 70-year historical data from the USA and Hungary. The model uses multiple features, including cigarette consumption and air pollution levels, and incorporates the time-lag effect of these factors. By analyzing historical trends, this project provides insights into the relationship between cigarette smoking, pollution, and lung cancer mortality.

The project utilizes a Bayesian approach, specifically a probabilistic programming model using PyMC, to estimate the impact of these factors over time, with the goal of predicting future trends in lung cancer mortality.

## Highlights:

#### ⭐ Lag features are engineered to capture the delayed and cumulative effects of smoke and pollution exposure on health:
- Time-lagged features were created to capture the delayed effects of cigarette consumption and pollution on lung cancer mortality.
- The lag features span from 25 to 35 years, as it is assumed that the effects of these factors on health outcomes may not be immediate.

### Model:
- **Probabilistic Programming**: The model was built using PyMC, a probabilistic programming library for Bayesian modeling.
- **Bayesian Linear Regression**: By extensive EDA, the model acknowledges that the relationship between the predictors (cigarette consumption and pollution) and the target (lung cancer mortality) is linear, but with added uncertainty in the form of priors.
- **Dirichlet Distribution**: A Dirichlet distribution was used to model the weights of the lagged variables.
- **Markov Chain Monte Carlo (MCMC)**: MCMC was used to sample the posterior distribution and estimate the model parameters.

## Performance
The model performs well with an average **root mean square error (RMSE)** of 3.23 and **R-squared** value of 0.98 in predicting lung cancer mortality. The model also demonstrates strong sensitivity to the lag effect of both cigarette consumption and pollution, indicating the long-term health impact of these factors.

- The posterior distributions of model parameters are estimated with high confidence (e.g., beta_cigarette coefficients 95% Highest Density Interval is [7.698, 8.337]).
- The model was validated with posterior predictive checks, showing strong alignment with the observed data.

## Future Work
This model can be expanded and improved in several ways:

- Adding more features: Additional factors such as socioeconomic data or medical advancements could be integrated to improve the model's accuracy.
- Model Tuning: The model can be fine-tuned with more sophisticated priors and by adjusting the lag range.
- Global Data: The model can be adapted to include data from other countries for comparative analysis.


## Installation

To run this project, you will need to install the following dependencies:

- Python 3.x
- `pymc` (for Bayesian modeling)
- `arviz` (for model diagnostics)
- `numpy` (for numerical operations)
- `pandas` (for data manipulation)
- `matplotlib` (for visualization)

## License
This project is licensed under the MIT License - see the LICENSE file for details.


