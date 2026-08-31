**12. Fundamentals of Probability**

1. describe an event and an event space.

2. describe independent events and mutually exclusive events.
3. explain the difference between independent events and conditionally independent events.
4. calculate the probability of an event for a discrete probability function.
5. define, describe, and calculate a conditional probability.
6. differentiate between conditional and unconditional probabilities.
7. explain and apply Bayes’ rule.

**13. Random Variables**

1. describe and differentiate a probability mass function from a cumulative distribution function and explainthe relationship between these two.
    - **概率质量函数**(probability mass function, PMF)：对某个离散型随机变量所有可能取值及其对应概率描述的函数
    - **累积分布函数**(cumulative distribution function, CDF)：随机变量$X$小于等于某特定值$x$的概率，即$F(x)=P(X\leq x)=∫_{-\infty}^xf(x)dx$
2. describe and apply the concept of a mathematical expectation of a random variable.
    - **数学期望**：以概率为权重，所有可能结果的加权平均 $E(X)=\sum p(x_i)x_i$
3. describe the four common population moments.
    - 一阶中心矩：**期望**(expectation)，$E(X)=\sum p(x_i)x_i$，即是中心矩也是非中心矩
    - 二阶中心矩：**方差**(variance)，$Var(X)=E[X-E[X]]^2$，
    - 三阶中心矩：**偏度**(skewness, S)：，反映数据分布的对称性，$S=\dfrac{E[X-E[X]]^3}{\sigma^3}$
    - 四阶中心矩:**峰度**(kurtosis, K)：衡量尾部的厚度，$K=\dfrac{E[X-E[X]]^4}{\sigma^4}$
4. explain the differences between a probability mass function and a probability density function.
    - **概率质量函数**(probability mass function, PMF)：对某个离散型随机变量所有可能取值及其对应概率描述的函数
    - **概率密度函数**(probability density function, PDF)：对某个连续型随机变量某一区间概率描述的函数
5. describe the quantile function and quantile-based estimators.
    - **分位数(quantiles)**：$\alpha$ 分位数是指能满足$P(X\leq q)=\alpha$ 的最小 $q$，即 $Q_X(\alpha)=F^{−1}(\alpha)$
6. explain the effect of a linear transformation of a random variable on the mean, variance, standard deviation, skewness, kurtosis, median, and interquartile range.
    - 一阶矩期望具有线性性质，$E[a+bX]=a+bE[X]$
    - 二阶矩方差不具有线性性质，$Var(a+bX)=b^2Var(X)$
    - 线性变换对三阶矩偏度的影响 $S(a+bX)=\left\{\begin{aligned}-S(X),b<0\\S(X),b>0\end{aligned} \right.$
    - 线性变换对四阶矩没有影响，$K(a+bX)=K(X)$

**14. Common Univariate Random Variables**

1. illustrate the key properties and applications of the following distributions: Bernoulli distribution, binomial distribution, Poisson distribution, uniform distribution, normal distribution, lognormal distribution, Chi-squared distribution, Student’s t distribution, F distribution, exponential distribution, and the Beta distribution.
    - 
2. construct mixture distributions, and explain the creation and characteristics of mixture distributions.
    - PDF 函数：$f(x)=\sum_{i=1}^nw_if_i(x),\sum_{i=1}^nw_i=1$
        - $w_i$ 表示概率，$f_i(x)$ 表示对应概率下的概率密度函数

**15. Multivariate Random Variables**

1. explain how a probability matrix can be used to express a probability mass function.
2. calculate the marginal and conditional distributions of a discrete bivariate random variable.
3. explain how the expectation of a function is calculated for a bivariate discrete random variable.
4. define covariance and explain what it measures.
5. explain the relationship between the covariance and correlation of two random variables, and how these are related to the independence of the two variables.
6. explain and illustrate the effects of applying linear transformations on the covariance and correlation between two random variables.
7. calculate the variance of a weighted sum of two random variables.
8. calculate the conditional expectation of a component of a bivariate random variable.
9. describe the features of an independent and identically distributed (iid) sequence of random variables.
10. explain and illustrate how the iid property simplifies the calculation of the mean and variance of a sum of iid random variables

**16. Sample Moments**

1. estimate the mean, variance, and standard deviation using sample data.
    - 样本均值 $\bar{X}=\dfrac{\sum_1^nX_i}{n}$
    - 样本方差 $S^2=\dfrac{\sum_1^n(X_i-\bar{X})^2}{n-1}$
    - 样本标准差 $S=\sqrt{\dfrac{\sum_1^n(X_i-\bar{X})^2}{n-1}}$
2. explain the difference between a population moment and a sample moment.
    - 总体参数是一个未知但客观存在的常数，是固定的
    - 样本统计量是随机变量，根据抽样数据的不同而不同，存在概率分布
3. differentiate between an estimator and an estimate.
    - 估计(estimate)：用于估计总体参数的一个值
    - 估计量(estimator)：用于计算估计的公式
4. describe the bias of an estimator and explain what the bias measures.
    - **偏误(bias)**：$Bias(\hat{\theta})=E(\hat{\theta})-\theta$
    - 若 $\hat{\theta}$ 无偏，则 $Bias(\hat{\theta})=0$
5. explain what is meant by the statement that the mean estimator is BLUE.
    - **BLUE(best linear unbiased estimator)**：同时满足无偏性、有效性，且关于样本数据是线性的统计量
6. describe the consistency of an estimator and explain the usefulness of this concept.
    - **一致性**(consistency)：随着样本容量的上升，样本统计量逼近总体参数的概率也会上升
    - **有效性**(efficiency)：在所有**无偏、线性**样本统计量中，方差最小的样本统计量。
7. explain how the Law of Large Numbers (LLN) and Central Limit Theorem (CLT) apply to the sample mean.
    - **大数定律**(LLN)：在大样本下样本均值会收敛到总体期望，即$\bar{X}=\dfrac{1}{n}\sum_1^nX_i\stackrel{a.s}{\longrightarrow}\mu$
    - **林德伯格-列维中心极限定理**(Lindberg-Levy CLT)：对于任意均为为$\mu$、方差为$\sigma^2$的总体，假设**简单随机抽样**计算出的样本均值为$\bar{X}$，样本容量为$n$，当$n(n\geq 30)$**较大**时，$\bar{X}$近似服从均值为$\mu$、方差为$\dfrac{\sigma^2}{n}$的正态分布
8. estimate and interpret the skewness and kurtosis of a random variable.
9. estimate quantiles, including the median, using sample data.
10. estimate the mean of two variables and apply the CLT.
11. estimate the covariance and correlation between two random variables.
12. explain how coskewness and cokurtosis are related to skewness and kurtosis.

**17. Hypothesis Testing**

1. construct an appropriate null hypothesis and alternative hypothesis, and differentiate between the two.
2. differentiate between a one-sided and a two-sided test and identify when to use each test.
3. explain the difference between Type I and Type II errors and how these relate to the size and power of a test.
4. explain how a hypothesis test and a confidence interval are related.
5. explain what the *p*-value of a hypothesis test measures, and calculate the *p*-value from a test statistic.
6. construct and apply confidence intervals for one-sided and two-sided hypothesis tests, and interpret the results of hypothesis tests with a specific confidence level.
7. identify the steps to test a hypothesis about the difference between two population means.
8. explain the problem of multiple testing and how it can lead to biased results.

**26. Machine Learning and Prediction**

1. explain the role of linear regression and logistic regression in prediction.
2. evaluate the predictive performance of logistic regression models.
3. describe and apply methods used to encode categorical variables.
4. discuss why regularization is useful, and compare the ridge regression and LASSO approaches.
5. illustrate how a decision tree is constructed and interpreted.
6. describe how ensembles of learners are built.
7. explain the intuition and processes behind the K-nearest neighbors and support vector machine methodsfor classification.
8. explain how neural networks are constructed and how their weights are determined.
9. compare the logistic regression and neural network classification approaches using a confusion matrix.