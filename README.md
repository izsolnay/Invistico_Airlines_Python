![Image of Delta seat back](https://github.com/izsolnay/Invistico-Airlines/blob/d214e7280d79106d7a9471c29886141bb83262ea/Inflight%20entertainment.png)
(*Image is of different airline seat used only for illustrative purposes. Invistico is not a real airline.)
# Invistico Airlines Customer Feedback Project
**Objectives** \
*1st case* \
Invistico Airlines is interested in learning if a better inflight entertainment experience leads to higher customer satisfaction. They would like the construction and evaluation of a model that predicts whether a future customer would be satisfied with their services given previous customer feedback about their inflight entertainment experience. 

*2nd case* \
The airline is interested in predicting whether a future customer would be satisfied with all of their services given previous customer feedback about their total flight experiences. The airline would like the construction and evaluation of a model that can accomplish this goal. They are also interested in knowing which features of the total flight experience are most important to customer satisfaction. 

**Deliverables** \
The data is sample size of survey responses from 129,880 customers. It includes data points such as satisfaction, class, flight distance, and inflight entertainment, among others. It is an in-house product.

*Models* \
(Since this project is a portfolio addition, the models are predetermined. Since this is a labelled data set, all models qualify as supervised.)

1st case: **Binomial logistic regression model** (1st notebook)\
In the first case, the airline is interested in <u>learning</u> whether a better *inflight entertainment* experience leads to higher customer *satisfaction*. The outcome (dependent y variable) is *satisfaction* a categorical Boolean variable (yes or no). The selected predicting (independent X variable) is inflight entertainment. (In point of fact, many of the variables in the data set could be employed for the model. However, the results from the following tree-based models suggest that *inflight entertainment* is the most predictive variable.)
For this task, a binomial logistic model (rather than linear) is appropriate. Binomial logistic regression is a statistical technique that models the probability of an event (*satisfaction*) based on one (or more) independent variables (*inflight entertainment*). The outcome must be a binary classification (satisfaction/dissatisfaction).  

2nd case: **Tree-based classification machine learning model** (2nd notebook)\
In the second case, the airline is interested in <u>predicting</u> whether a future customer would be satisfied with their flight experience given previous customer feedback. They are also interested in knowing which features of their flight experience are most predictive of that satisfaction. Decision trees are classification models that can handle all of the types of variables this data set contains (categorical, discrete, and continuous). They make predictions for a target variable based on multiple variables (features). Because decision trees return a weighted map of possible outcomes to any series of related choices, the airline can use these findings to allot their available resources.

For this 2nd case, 3 tree based models are trained, tuned, evaluated, and compared for the most predictive power. The most predictive will be tested on the unseen test data.\
  1.	**Simple decision tree**: can handle collinearity and has no assumptions about data distribution. This works well for this data set, since its variables have highly uneven distributions and scales.
  2.	**Random Forest**: these models leverage randomness by combining the results of many models to help make more reliable final predictions. These predictions have less bias, and lower variance than other standalone models. They are also very scalable (thus can handle outliers easily, which is also a factor in this data set) and less susceptible to overfitting.
  3.	**Gradient Boosting (XGBoost)**: these models have a high accuracy rate, work well with missing data (which this data set has), are scalable, and can provide a weighted feature importance chart. However, as they are considered black-boxes, their steps cannot be seen (the trees cannot be produced).

The goal will be to utilize the best decision tree model to predict whether or not a customer will be *satisfied*(y) with their flight experience based on multiple variables in the data set(Xs) and discover which variables are most predictive of that outcome.

All code is located at: https://github.com/izsolnay/Invistico_Airlines_Python
