## Generalized Linear Models

We are not able to perform satisfactory regression analysis with the classical linear model when the distribution of the response variable is considerably skewed. Although, we can apply transformations that can approximate a symmetric distribution, it is often advantageous to apply, for example, a gamma regression model to the original response variable.

Within a broad framework, GLMs unify many regression approaches with response variables that do not necessarily follow a normal distribution, including, for example, the logit model for binary response variables as well as the classical linear regression for normally distributed reponse variable.

### Binary Regression

Say we have a response variable $y$ with $k$ covariates $x_1...x_k$ and $y \in \{0, 1\}$ while the covariates can take binary or continuous values.

The classical linear model $$\mathbb{E}(y_i) = \mathbb{P}(y_i = 1) =  \pi_i = \bf{x_i}^{T}\bf{\beta}$$ won't work since LHS is bound between $0$ and $1$, while the RHS is not. Therefore, we transform the RHS to be bound in $[0, 1]$. Thus, 
$$\pi_i = h(\eta_i) \ \text{where} \  \eta_i = \bf{x_i}^{T}\bf{\beta}$$

In the GLM lingo, $g = h^{-1}$ is called the _link function_ ($\eta_i = h^{-1}(\pi_i)$).

