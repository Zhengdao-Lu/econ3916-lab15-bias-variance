# econ3916-lab15-bias-variance
# Objective

I tested how polynomial complexity affects prediction error and used cross-validation to choose a degree.

# Methodology
- I used simulated data with a known true curve and estimated squared bias and variance from 200 fresh samples at each of six polynomial degrees.
- I compared training error with error on 2,000 new points for degrees 1 to 15.
- I used 5-fold cross-validation to choose a degree and examined how the error varied across folds.
- I used nested cross-validation to estimate the error of the degree-selection process.
- I wrote kfold_mse() and used it to compare degrees 4 and 5 with 10 folds.

# Key findings
Variance rose from 0.0180 at degree 5 to 0.0994 at degree 15. Held-out error was lowest at degree 5. The 5-fold CV chose degree 4 with an MSE of 0.1401, while nested CV estimated 0.2070. With 10 folds, the MSE was 0.1409 for degree 4 and 0.1457 for degree 5, so degree 4 still ranked lower.
