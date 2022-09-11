---
layout: single
title:  "Introduction to Machine Learning"
comments: true
summary: "Introduction to Arduino and a simple tutorial of turning on a LED"
categories: [ML]
toc: true
author_profile: false
---

## Polynomial Curve Fitting


<!-- $$ {X}_{0} $$ (works)
$$ X_0 $$ (works)

\begin{equation}
\begin{aligned}
  {\sigma}_{1} =  
  \begin{pmatrix}
    0 & 1 \\\\\\\\
    1 & 0
  \end{pmatrix} 
\end{aligned}
\end{equation} -->

The goal is to find a function that fits the data. We use a polynomial function of the form

\begin{equation} 
y(x, w) = w_0 + w_1x + w_2x^2 + ... + w_Mx^M = \Sigma_{j=0}^{M} w_jx^j
\end{equation}

where M is the order of the polynomial and $w_0, ..., w_M$ are the polynomial coefficients denoted by the vector $w$.
We want to find the values of the coefficients, $w$. Therefore, the equation is linear about $w$.
The values are determined by fitting the equation to the training data set.
Let the target values be $t = [t_1, ..., t_N]^T$ of a dataset $x = [x_1, ..., x_N]^T$.
$\hat{t}$ is predicted target values by the function, $y(x, w)$.
We can evaluate the function by getting the differences between $\hat{t}$ and $t$. The differences are the errors.
Having small errors means the function predicts the target value precisely. Hence, we want to minimize the sum of the errors and find w that minimizes the sum.
The sum of errors are the following
\begin{equation}
E(w) = \frac{1}{2} \Sigma_{n=1}^N {y(x_n, w) - t_n}^2
\end{equation}

If we only use some data points in the training data set, the result will be not accurate. This is called under-fitting. On the other hand, if we use all the data points, the function will predict the target values correctly. This is over-fitting. Under-fitting poorly represents the pattern of the training data set and over-fitting overly represents the pattern. If the machine learning model overly represents the pattern, when we feed a new input data point, the model is not flexible enough to predict the target value of the new input.

