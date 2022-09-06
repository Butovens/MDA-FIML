# Missing Data Analysis: Full Information Maximum Likelihood (FIML)
> Probably the most pragmatic missing data estimation approach for structural equation modeling is full
information maximum likelihood (FIML), which has been shown to produce unbiased parameter
estimates and standard errors under MAR and MCAR (Enders & Bandalos, 2001). 
>
> [...]
>
> There is good evidence to suggest that using modern missing data estimation approaches
may be advantageous even if missingness is initially nonignorable (i.e., MAR assumptions have not
been met) provided correlates of missingness, referred to as auxiliary variables, are included in the
model.
>
> -- <cite>Newsom Psy 523/623 Structural Equation Modeling, Spring 2020</cite>

## This is an example of FIML implementation in R.

The substantive goal is to fit a multiple regression model that predicts intentions to use steroids from the following predictors: knowledge of steroid effects, knowledge of testosterone effects, and knowledge of supplements. 

The analysis model is: mayuse = b0 + b1(sterknow) + b2(testknow) + b3(suppknow) + e

Here we want to compare and contrast the estimation of the regression model above (without the auxiliary variables using FIML) with the same model using the saturated correlates approach to incorporate the auxiliary variables into the analysis.

We will take as auxiliary variables:

* **attuse** (attitudes toward steroid use)
* **streneff** (strength training efficacy)
* **teaminfo** (team as an information source)
* **coachtol** (coach tolerance of steroid use)
* **esteem** (self‐esteem)
* **impuls** (impulsivity)
