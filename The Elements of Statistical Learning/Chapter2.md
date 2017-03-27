# The Overview of Supervised Learning


* What is Supervised Learning
	* A set of variables called **inputs**.
	* In statistical literature the inputs called **predictors**, more called **independent variable**.
	* In pattern recognition literature, called **features**.
	* **Inputs** has some influences on **outputs**.
	* **Outputs** is called **response** or **dependent variable**.
	* A machine learning task with the training data consist of a set of input and output is called supervised learning.
	
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
	* Yhat = X.T * β, gradient dY = β
	* Linear Model: *least squares* RSS(β) = (y - Xβ).T * (y - Xβ)
		* Form a desicion boundary 
		* The overlap of region is inevitable.
		* A optimal desicion boundary is not linear, but disjoint
	
* K-Nearest-Neighbor Methods
	* Yhat(xi) is the **mean of k cloest points to xi in the training set**.
	* 1-Nearest-Neighbor of Yhat(xi) is xi itself in the training set.
	* 1 parameter, the number of k.
	* Err on training data with k = 1 is always 0. Thus,  cannot use *MSE* to pick up the k
	* *effective* number is N/k, greater than p, and decreases with incresing k.
	

* Least Squares VS KNN
	* Linear Squares:
		* Desicion boundary is smooth and stable to fit.
		* Assumpation relies on the desicion boundary
		* low variances and potentially high bias.
	* KNN:
		* Desicion boundary is useless.
		* Does not rely on the decision boundary, can adapt to any situation.
		* Depend on the input points and their particular positions
		* Wiggy, unstable -- high variance, low bias	
	* Two senarios:
		* The training data in each class were generated from bivariate Gaussian distributions with uncorrelated components and different means. (Linear models are more situable)
		* The training data in each class came from a mixture of 10 low- variance Gaussian distributions, with individual means themselves distributed as Gaussian. (KNN is more situable)

* Statistical Decision Theory
	* The deduction is on page 18.
	* Loss function, L(Y, f(X)) = (Y-f(X))^2
	* EPE, excepted prediction error, = E((Y-f(X))^2)
	* The solution is f(x) = E(Y|X = x)
	* E.g. In KNN, the f(x) = Avg(yi|xi ∈ Nk(x)), where Nk(x) means the k cloest neighborhood points of x. N, k -> ∞  such that k/N -> 0, therefore, f(x) -> E(Y|X = x)
	
	
	
	
	