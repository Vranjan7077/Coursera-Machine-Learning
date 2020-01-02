## Evaluating a Hypothesis ##
Once we have done some trouble shooting for errors in our predictions by:

1)  Getting more training examples<br/>
2)  Trying smaller sets of features<br/>
3)  Trying additional features<br/>
4)  Trying polynomial features<br/>
5)  Increasing or decreasing λ

We can move on to evaluate our new hypothesis.

A hypothesis may have a low error for the training examples but still be inaccurate (because of overfitting). Thus, to evaluate a hypothesis, given a dataset of training examples, we can split up the data into two sets: a training set and a test set. Typically, the training set consists of 70 % of your data and the test set is the remaining 30 %.

The new procedure using these two sets is then:

1)  Learn Θ and minimize Jtrain(Θ) using the training set
2)  Compute the test set error Jtest(Θ)

## Model Selection and Train/Validation/Test Sets ##
Just because a learning algorithm fits a training set well, that does not mean it is a good hypothesis. It could over fit and as a result your predictions on the test set would be poor. The error of your hypothesis as measured on the data set with which you trained the parameters will be lower than the error on any other data set.

Given many models with different polynomial degrees, we can use a systematic approach to identify the 'best' function. In order to choose the model of your hypothesis, you can test each degree of polynomial and look at the error result.

One way to break down our dataset into the three sets is:

. Training set: 60%<br/>
. Cross validation set: 20% <br/>
. Test set: 20%

We can now calculate three separate error values for the three different sets using the following method:

1)  Optimize the parameters in Θ using the training set for each polynomial degree.
2)  Find the polynomial degree d with the least error using the cross validation set.
3)  Estimate the generalization error using the test set with Jtest(Θ(d)), (d = theta from polynomial with lower error);
This way, the degree of the polynomial d has not been trained using the test set.
