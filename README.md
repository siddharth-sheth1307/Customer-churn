# Customer-churn
Predict risk of churn for individual customers and recovery
Motivation : 
Customer churn is a major challenge and a high concern for most large companies. Due to its direct effect on the reveneus of big companies, especially the Telecom field, tools are being developed to predict the risk of potential customer churn and thereby take necessary actions to reduce this churn 

I begun by collecting the raw data required from Kaggle open source and processed the data for analysis. The data had to be accounted for missing values
I continued by conducting exploratory data analysis of the dataset to better understand the patterns in the data.
•	Exploratory data analysis
A few important insights gained were the following: 
a)	A lot of customers are either 1-2 months/ over 6 years in their contracts 
b)	New customers were subject to month-month contracts while long term customers were bound to a 2-year contract
c)	A high number of customers with Phone service, TV streaming and Internet Service were present
d)  Churn risk is high when there’s a high monthly charge
e)  Churn risk is high for low total charges
 
•	Data preparation for modelling 
1.	The dataset was split into train and test sets
2.	Categorical variables were transformed using Dummy encoding and numerical variables were transformed using MinMax scaler to normalize them and account for outliers
3.	Feature selection was done using Recursive feature elimination through cross validation to select best features that can be deployed into the model
 
A total of 19 features were selected for modelling based on the technique above

•	Model deployment 
Logistic regression, Support vector machine, K-nearest neighbours, Naïve Bayes, Decision tree, Random forest and XG boost models were developed

Random forest boosting algorithm resulted in highest accuracy score

The feature importance in all algorithms were analysed and the studies were as follows: 
Negative relation means that likeliness of churn decreases with that variable 

1.	From random forest algorithm, monthly contract, tenure and total charges are the most important predictor variables to predict churn.
2.	A 2-year contract greatly reduces the risk of churn 
3.	A Fiber-optics connection highly increases the rate of churn 
4.	Total charges as opposed to monthly charges reduce the risk of churn which indicates when customers are required to pay in a single shot they stay longer 

Strategies for retention
1.	From the predictive model and earlier EDA, we see that a high monthly charge is a huge risk for churn. 
Strategy: The team can offer customers an option to pay in installments/long term-bulk payments
2.	The company could bind the customer to a long-term contract. 
Strategy: Offer various marketing incentives like cheaper rates, additional services(Wifi, Movie, etc) , gift cards
3.	Further research on why customers having Fibre-optics connection have high risk 
(Possibilities: Poor services, unstable connection, low speeds?)


