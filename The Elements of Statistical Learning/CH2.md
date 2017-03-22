# The Overview of Supervised Learning


* What is Supervised Learning
	* A set of variables called **inputs**.
	* In statistical literature the inputs called **predictors**, more called **independent variable**.
	* In pattern recognition literature, called **features**.
	* **Inputs** has some influences on **outputs**.
	* **Outputs** is called **response** or **dependent variable**.
	
* Different variable types
	* Qualitative(定性的) variable are called **categorical** or **discrete** variables.
	* Quantitative(定量的) variable are called **continued**, measured in number and **more close in number means more close in nature**.
	* Predict the qualitative variable is __classification__ and we use the term __regression__ for predicting the quantitative variable.
	* A third variable type is __ordered categorical__, such as small, medium and large.
	
* Denote of variable
	* Use __X__ to denote the input variable.
	* Use __Y__ for quantitative outputs and __G__ (group) for qualitative outputs.
	* xi means the column number of matrix
	* jth row of the matrix is the Xj of the transpose matrix of X.
	* For example, we have N inputs and P features, the X is NxP.
	* Use __Y-hat or Yhat__ represent the prediction of output that is represented by value
	* Use __G-hat or Ghat__ represent the categorical predictions
	* For binary categorical prediction we can use [0, 1] to represent and use __Yhat__
	* Y = X.T * coefficients 