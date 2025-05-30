# Data Science Programming Task
This repository contains the Data Analysis of Stackoverlow Posts for two tags (i.e., “wordpress” and “drupal”)  within a 6-month period (i.e., "01/2021-06/2021”). The repository contains the data extracted using big query api and the jupyter notebooks that are needed to perform an indepth analysis on the csv files of the two tags (e.g., “wordpress” and “drupal”). 

The following are the two types of Data Analysis techniques which were performed: 

1. Generated Shaded Density Plots with Rug Plot to understand the differences in distribution of the five different metrics (i.e., Answer Count, Comment Count, Favorite Count, View Count, Score) between the posts of the two tags (i.e.,  “wordpress” and “drupal”)

2. Generated Time Series Plots to understand the topical trend of the five different metrics (i.e., Answer Count, Comment Count, Favorite Count, View Count, Score) over the creation Date intervals between the posts of the two tags (i.e.,  “wordpress” and “drupal”)

# Required tools and packages
The following tools were installed on the machine where the scripts were originally executed:
* Python 3.6.8
* Jupyter Notebook

In addition, the following Python packages were installed:
* pandas
* matplotlib
* seaborn
* datetime
* bq_helper

# Data Extraction

1. Obtain the SO posts, i.e., questions and their answers, for two tags (i.e., “wordpress” and “drupal”) within a given time period (i.e., "01/2021-06/2021") using biq query. 
2. Extracted for each post the mentioned id, creation_date, tags, answer_count, comment_count, favorite_count, view_count, and score. 
3. Generated csv files for the wordpress and drupal tags with one line per post, where each line contains an identifier for a post (i.e., id) and the values for the 5 chosen metrics (i.e., answer_count, comment_count, favorite_count, view_count, and score)

The Code for Data Extraction process is <a href="https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/Stackoverflow_DataExtract.ipynb">here</a>

# Data Analysis Results

The Code for Data Analaysis part is <a href="https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/StackOverFlow_DataAnalysis.ipynb">here</a>  

## Analysing the differences in distribution of the 5 metrics between the posts of the two tags

With the Shaded Density Plots of the 5 metrics (i.e., answer_count, comment_count, favorite_count, view_count, and score) mentioned below , we come to the conclusion that wordpress tag conatin higher density of metric distributions compared to drupal tag. In Addition, the Rug plots shows that the range of metric values of wordpress tag is more wide compared to drupal tag.

![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Shaded%20Density%20Plot%20with%20Rug%20Plot%20for%20Answer%20Count.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Shaded%20Density%20Plot%20with%20Rug%20Plot%20for%20Comment%20Count.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Shaded%20Density%20Plot%20with%20Rug%20Plot%20for%20Favorite%20Count.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Shaded%20Density%20Plot%20with%20Rug%20Plot%20for%20View%20Count.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Shaded%20Density%20Plot%20with%20Rug%20Plot%20for%20Score.jpg)

## Analysing the Time Series Trend of the 5 metrics between the posts of the two tags over the Fixed Sliding intervals (i.e., Weekly basis)

With the time series graph of the 5 metrics (i.e., answer_count, comment_count, favorite_count, view_count, and score) mentioned below, we come to the conclusion that wordpress tag conatins higher concentration of all the 5 metric values compared to drupal tag over the the sliding intervals of 7 days. With regards to the posts containing wordpress tag, the metrics such as Answer Count, View Count, and Score shows an overall decreasing trend over the Creation Date intervals. Moreover, the comment_count and favorite_count of posts containing wordpress tag shows high fluctuation in spikes with no proper trend observed for posts created from January to June. 

In case of SO posts containing drupal tag, all the five metrics (i.e., answer_count, comment_count, favorite_count, view_count, and score) doesnot show any major high count  compared to wordpress tag. In addition, the overall trend of all the 5 metrics for drupal containing posts created during the span of 6 months shows steadiness with low deviation and low count.


![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Answer%20Count%20Trend%20of%202%20tags.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/View%20Count%20Trend%20of%202%20tags.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Score%20Trend%20of%202%20tags.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Comment%20Count%20Trend%20of%202%20tags.jpg)
![](https://github.com/jaskirat111/StackoverFlowDataAnalysis/blob/main/figures/Favorite%20Count%20Trend%20of%202%20tags.jpg)

