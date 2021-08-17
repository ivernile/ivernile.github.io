---
layout: post
title: Logistic Regression
published: true
---
Logistic Regression was utilized in the biological sciences in early
twentieth century. It had been then utilized
in many science applications.Logistic regression is named for the function used at the core of the method, the logistic function.Logistic Regression is
employed when the dependent variable(target) is categorical.
For example,

-To predict whether an email is spam (1) or (0)

-Whether the tumor is malignant (1) or not (0)

Consider a scenario where we would like to classify whether an email is spam or not. If we use linear regression for this
problem, there is a requirement for fixing a threshold, which is basis of classification in this scenario. Suppose, if the particular class is malignant, and the continuous  value predicted is 0.4 with threshold value as 0.5, the data point are going to be classified as not malignant which may cause serious consequence in real time.

From this instance , it is often inferred that linear regression is not  suitable for classification problem. linear regression is unbounded i.e predicts a value that is continuous in nature , so this brings logistic regression into
picture where output value strictly ranges from 0 to 1.

### **Simple Logistic Regression**

**Here is the mathematical model of logistic regression**

Output = 0 or 1

Hypothesis ===> Z = WX + B

hΘ(x) = sigmoid (Z)

**Sigmoid Function** 

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092524/sigmoid_fxn_litvi5.png)

Figure 1: Sigmoid Activation Function

As ‘Z’ goes on to infinity, Y(predicted) will become 1 and if ‘Z’ goes to negative infinity, Y(predicted) will become 0. One can think of sigmoid function as  an object though which any number upon entry can take either the form of zero or one.

### **Analysis of the hypothesis**



The output from the hypothesis is the estimated
probability. This is often used to infer how confident can predicted
value be to actual value when given an input X. Consider the below
example,
Based on the x1 value, let’s say we obtained the estimated
probability to be 0.8. This tells that there&#39;s 80% chance that an email is going to be spam.

Mathematically this can be written as,

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092521/mathemarical_representation_idsuas.png)

Figure 2: Mathematical Representation

This justifies the name ‘logistic regression’. Data is fit
into linear regression model, which is then acted upon by a logistic function predicting the target categorical variable .

### **Types of Logistic Regression**

1. Binary Logistic Regression

The categorical response has only two 2 possible outcomes.
Example: Spam or Not

2. Multinomial Logistic Regression

Three or more categories without ordering. Example: Predicting
which food is preferred more (Veg, Non-Veg, Vegan)

3. Ordinal Logistic Regression
Three or more categories with ordering. Example: Movie rating
from 1 to five

### **Decision Boundary**

To predict which class a data point belongs, a threshold is
often set. Based upon this threshold, the obtained estimated
probability is assessed into classes.
Say, if predicted_value ≥ 0.5, then classify email as spam else as
not spam.
Decision boundary can be linear or non-linear. Polynomial
order are often increased to get complex decision boundary.

### **Cost Function**

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092520/cost_function_of_logistic_regression_uuk3fp.png)

Figure 3: Cost Function of Logistic Regression


Why cost function which has been used for linear can&#39;t be used for
logistic?

Linear regression uses mean squared error as its cost function.
If this is used for logistic regression, then it will be a non-convex function of parameters (theta). Gradient descent will converge into global minimum as long as the function is convex.

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092519/convex_and_non_convex_functions_jkepda.png)

Figure 4: Convex and non-convex cost function

### **Cost function explanation**

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092529/cost_function_explanation_xf3dls.png)

Figure 5: Cost Function part 1

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092522/cost_function_explanation_part_2_d7sveo.png)

Figure 6: Cost Function part 2

### **Simplified cost function**

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092525/simplified_cost_function_gs675n.png)

Figure 7: Simplified Cost Function


### **Why this cost function?**

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092528/maximum_likelyhood_explanation_part_1_fznvrp.png)

Figure 8: Maximum Likelihood Explanation part-1

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092528/maximum_likelyhood_explanation_part_2_rggwt5.png)

Figure 9: Maximum Likelihood Explanation part-2

This negative function is because when we train, we need to maximize the probability by minimizing loss function. Decreasing the cost will increase the maximum likelihood assuming that samples are drawn from an identically independent distribution.

### **Deriving the formula for Gradient Descent Algorithm**

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092527/gradient_part_1_utlzbh.png)

Figure 10: Gradient Descent Algorithm part 1

![](https://res.cloudinary.com/dra6leodq/image/upload/v1629092528/gradient_part_2_fzngj6.png)

Figure 11: Gradient Descent part 2






This post is written inorder to fulfill assignment requirement of Machine learning course and has been reused from 

https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc.
