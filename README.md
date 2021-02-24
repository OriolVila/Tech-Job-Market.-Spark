# Tech-Job-Market-Spark Project
Analysis of the Tech Job Market wih Spark SQL &amp; DataFrame APIs

**INTRODUCTION**

Hiring data experts has become a challenging task for tech firms since their business demand a high number of data specialists. A way to attract talent can be paying higher wages. However, this
is just one of the many factors, and probably not the most relevant one. Firms and employees understand that work is
much more than giving your time in exchange of money. Although people might have different perspectives
on the relevance of the factors that affect our overall job satisfaction, some of the most predominant are career opportunities, location, benefits, values, sector, management style and work-life balance.

**DATASET**

To find the hidden patterns of the job market for tech professionals we use a dataset with data
scrapped from Glassdoor by Andre Sionek which is available on Kaggle (link to the dataset attached in the code). It contains information of review of current and former employees with experience in the following fields: data-scientist, software-engineer, data-analyst, research-scientist, business-analyst, product-manager, project-manager, data-engineer,
statistician, dba, database-engineer and machine-learning-engineer. The dataset has reviews from 2008 to
2019 and it initially contained 28 variables and 946168 rows. After transforming some variables and
removing null rows, the final dataset has 17 variables and 236639 rows.

**GOAL**

The objective of the present analysis is threefold. Firstly, we analyse the popularity of different types of jobs related to data. This implies detecting the cities with more tech employees, the most popular job titles and
the jobs with the highest overall satisfaction. Additionally, the scope of Data Scientist and Data Analyst is
compared to the rest of market. Secondly, we go at the firm level and we look at companies which have more
reviews from current employees. We start by ranking them by the number of employees and then we
explore which firms obtain the best and the worst ratings according to different criteria (overall, work-life
balance, benefits and opportunities). Lastly, we focus on Amazon, one of the key players as we will see in
the next lines, and study the most common pros and cons that their tech employees review on Glassdoor by extracting the most repeated words on their reviews.

**ANALYSIS**

*Setup* From [Cell 1 to 15] we create our environment setup, an Spark Session and we apply transformations to the DataFrame in order to clean it. The result of this process is a temporal view, named "filtered_v, with 236639 rows and 17 variables.

*A. Types of job*
From [Cell 16 to 21] we use the SQL API to do the queries that will answer our questions about the characteristics of the most relevant job titles.

From [Cell 22 to 27] we go to a firm level and detect the big players in the market.

From [Cell 28 to 32] we create a DataFrame containing only the reviews from Amazon's employees and we use the DataFrame API to explode each word from the pros and cons section, and create a new row for each of the words. Next, we select the most repeated words to get an idea of what it is like to work at Amazon as a tech expert.


**CONCLUSIONS**

We have seen that job reviews from tech-related employees are rapidly growing and it is likely that the
demand for such professionals will keep increasing in the next years. The overall rating is 3.88 out of 5 for the
sector and Data Analysts and Data Scientists have an overall rating of 4.06, which is slightly higher.
Singapore is the city that has attracted more tech employees in the last years and the most reviewed job
title is Software Engineer. Nonetheless, Software Engineers do not seem to be the ones with higher job
satisfaction. Cloud Support Associates actually have an insuperable overall satisfaction, 5 out of 5.

Regarding the key players in the market, Amazon, Oracle, Dell Technologies, Microsoft and Google are the
companies which have more reviews from current employees. The five firms together sum 8.13% of all the
reviews. However, these companies are not the ones with the highest overall rating. The top 3 firms with
higher rating are Spotify, followed by Air Asia and Zalando. On the other hand, the firms with worst rating
from their current employees are Sqlink Group, Mitra Int. and Dyson.

Finally, we put our attention on Amazon, on of the biggest players. We analysed the most repeated words in the reviews of its employees and concluded that Amazon has a good working environment and excellent opportunities to grow and learn but it is difficult to have a good work-life balance.
