# Movie Revenue Prediction Considering Gender Diversity and Star Power
This is Team Unsupervised Learner's repo of our term project for *DS-GA 1001 Introduction to Data Science* at New York University Center for Data Science. **Read our final report here: [Project Write-Up](https://github.com/mginabluebox/movie_revenue_prediction/blob/master/Project%20Write-Up.pdf)**. 

<p align="center">
  <img src="https://github.com/mginabluebox/movie_revenue_prediction/blob/master/graphs/actor_log_revenue_over_years.png"><br>
  <i>Figure 1: Average log revenue of starred movies in a 5-year running window</i>
</p>

# Abstract
Every business strives to predict consumer behavior and deliver what their consumers want. In 2019, the movie industry grossed over $100 billion, but the astronomical costs of producing a movie mean that even experienced and well-funded studios can struggle to produce multiple consistently profitable films each year. According to our data, the average major studio produced only 1.8 films per year at an average cost of $40.5 million per film. Through machine learning and data analysis techniques, we hope to identify key factors that predict box office success, and how changes in them affect a movie’s revenue. 

We also want to focus on two initiatives: gender diversity and star power. Since gender inequality in the entertainment industry has come under the spotlight with the advent of #MeToo movement, we are curious about how the level of gender diversity in a movie would affect its financial success. If we could identify financial incentives to increase female representation, it could accelerate the push for equality. Moreover, we research whether the film leads' star power influences audiences’ viewing decision.

Our project is innovative on feature engineering. We created trend features to represent starpower using historical movie revenue data, which captures the variations in an actor's popularity over time. We further defined having award-winning actors as another aspect of starpower by cross-referenced an Oscars dataset. To represent gender diversity, we used the proportion of female actors in each movie as a proxy. On these basis, we built and compared performances of several supervised learning models including SVR, decision tree, random forest, gradient boosted decision tree and linear regressions on a train/val/test split based on movie release years. We examined the effects of our variables of interests through our linear models' results. 

# Repo Description 
Our model results are in the [results](https://github.com/mginabluebox/movie_revenue_prediction/tree/master/results) folder. Our fully-executed jupyter notebooks are in the [code](https://github.com/mginabluebox/movie_revenue_prediction/tree/master/code) folder. Some feature engineering results such as top 100 actor lists are in the [feature](https://github.com/mginabluebox/movie_revenue_prediction/tree/master/feature) folder and all plots in our final report can be found in [graphs](https://github.com/mginabluebox/movie_revenue_prediction/tree/master/graphs). Final data used in our models and outputs from our preprocessing step can be found in [data](https://github.com/mginabluebox/movie_revenue_prediction/tree/master/data).

# Data
We used data from Kaggle's [The Movie Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset) and [The Oscar Award, 1927 - 2020](https://www.kaggle.com/unanimad/the-oscar-award).

# Credits
[**Charlotte Ji**](https://www.github.com/mginabluebox)
- Contributed to data cleaning and understanding, plotted revenue over years
- Created genre and collection variables 
- Generated correlation matrix, mutual information and VIFs and their plots and tables
- Built and tuned OLS, ridge regression and random forest models 
- Interpreted model results and wrote respective parts of the write-up 

[**Hengjiali Xu**](https://www.github.com/HengjialiXu)
- Created log budget, log revenue, production company class, title length variables.
- Created graph of log budget and EDA
- Created baseline models
- Trained and tuned decision tree regressor and SVR 
- Wrote some parts of the write-up and assisted in write-up editing

[**Mars Wei-Lun Huang**](https://github.com/ntu519198)
- Created is_topk_director/actor, directors’ and actors’ log(revenue) feature variables.
- Created graph of the trend of actors’ log(revenue) and EDA
- Trained and Tuned Hyper-parameters for Gradient Boosting Regression Tree
- Added explanation for target variable
- Assisted in model explanations

**John Fitzpatrick**
- Assisted with planning and scheduling
- Created gender_score and has_oscar_winner feature variables
- Created some of the graphs and EDA
- Consulted on model selection process
- Wrote much of the first draft of the report and helped with editing
