# DSI-23 Capstone Project: Analysis on COVID-19 Pfizer/BioNtech Vaccine Tweets (Sentiment Analysis & Topic Modelling)

## Introduction

[COVID-19 is the disease caused by a new coronavirus called SARS-CoV-2](https://www.who.int/emergencies/diseases/novel-coronavirus-2019/question-and-answers-hub/q-a-detail/coronavirus-disease-covid-19). The novel virus was first identified in Wuhan, China, in December 2019; it spread to other parts of mainland China and eventually around the world. The World Health Organization (WHO) declared a Public Health Emergency of International Concern on 30 January 2020, and a pandemic on 11 March 2020. 

Since 2021, variants of the virus have emerged or become dominant in many countries, with the Delta, Alpha and Beta variants being the most virulent. As of 31 August 2021, more than 217 million cases and 4.51 million deaths have been confirmed, making it one of the deadliest pandemics in history. 

The first mass vaccination programme started in early December 2020. The Pfizer/BioNtech vaccine was the first to be listed for WHO Emergency Use Listing (EUL) on 31 December 2020.

Due to the extensive data available on the Pfizer/BioNtech vaccine (compared to other vaccines), this project looks to analyze tweets about the Pfizer/BioNtech vaccine, mainly on the following:
1. Sentiment analysis on the Pfizer/BioNtech vaccine tweets, to understand the overall global sentiment. 
2. Topic modelling within each sentiment, to further understand the possible reasons behind the sentiment. 

## Problem Statement

Through analyzing tweets on the COVID-19 Pfizer/BioNtech vaccine, this project aims to understand the overall global sentiment across time on the Pfizer/BioNtech vaccine. In addition to the sentiment analysis, topic modelling will be explored to further break down the discussion topics within each sentiment group. The goal is to identify potential interventions for Pfizer/BioNtech to take, in order to speed up the global vaccination progress.

## Data Dictionary

The datasets involved in this project are as follows. 

|Dataset|Description|
|:---|:---|
|[`vaccination_all_tweets.csv`](../assets/vaccination_all_tweets.csv)|The original dataset retrieved from [Kaggle](https://www.kaggle.com/gpreda/all-covid19-vaccines-tweets/metadata) (version 90), containing tweets about all COVID-19 vaccines.| 
|[`pfizer_tweets.csv`](../assets/pfizer_tweets.csv)|Dataset containing tweets about the Pfizer vaccine, after performing sentiment analysis.| 

|Feature|Type|Description|
|:---|:---:|:---|
|user_name|*str*|User name of the Twitter account.| 
|user_location|*str*|User location of the Twitter account.| 
|user_description|*str*|User description of the Twitter account.| 
|user_created|*date*|Date when the Twitter account was created.| 
|user_followers|*int*|Number of the followers of the Twitter account.| 
|user_verified|*bool*|Verification status of the Twitter account (True/False).| 
|date|*date*|Date when the tweet was posted.| 
|text|*str*|Content of the tweet.| 
|hashtags|*list*|Hashtags used in the tweet.| 
|source|*str*|Source / device where the tweet came from.| 
|retweets|*int*|Number of retweets of the tweet.| 
|favorites|*int*|Number of favorties (equivalent to likes) of the tweet.| 
|is_retweet|*bool*|Whether the tweet is a retweet (True/False) | 
|sentiment|*str*|The sentiment category of the tweet (Positive/Neutral/Negative)| 

## Results

![sentiment_distribution.png](https://github.com/JeffreyPrasetio/DSI-23-Capstone-Project/blob/main/visuals/sentiment%20distribution.png)

Overall, most tweets on the Pfizer/BioNtech vaccine had neutral sentiment, followed by positive and lastly negative.

In the positive tweets, people mainly talked about their experiences on taking the vaccine, the FDA approval, and the Johnson & Johnson vaccine.

In the negative tweets, people talked about the Astra Zeneca vaccine, death cases, and vaccine failures.

Lastly, in the neutral tweets, people talked had general discussions on COVID-19 vaccines, getting vaccinated, and comparisons between the different vaccines.

NOTE: Refer to the html files in the visuals folder for interactive plots generated from topic modelling.

## Conclusions & Recommendations

From the uncovered results, we can identify potential interventions for Pfizer/BioNtech to take in order to speed up the global vaccination progress (and also drive revenue by increasing their vaccine sales).

1. Although the Pfizer/BioNtech vaccine received the FDA approval on 23 Aug 2021, it was preceded with negative sentiment about how the vaccine is less effective against the Delta variant (Israel outbreak). In order to leverage on the FDA approval status, the company will have to address this controversy - if it's true, perhaps more R&D will have to be invested into a 'vaccine upgrade'. From the sentiment analysis, we saw that the highest negative spike was due to the Delta variant outbreak in India. As such, if Pfizer/BioNtech is able to effectively combat the Delta variant, that would highly increase the vaccine's marketability. 

2. As seen from the sentiment distribution within each country, there is no obvious country with tremendously positive sentiment towards the Pfizer/BioNtech vaccine. As such, when it comes to location targeting, the company should look towards countries with the large populations and lowest vaccination rates. There is higher urgency in those countries and their government bodies will be more compelled to listen.

3. The Johnson & Johnson vaccine was received positively [due to its effectiveness against the Delta variant](https://www.jnj.com/positive-new-data-for-johnson-johnson-single-shot-covid-19-vaccine-on-activity-against-delta-variant-and-long-lasting-durability-of-response). In return, the Astra Zeneca vaccine has had [a negative history of problems](https://www.cnbc.com/2021/03/25/astrazeneca-covid-vaccine-all-the-issues-and-problems-the-shot-has-faced.html). The company should study other vaccine manufacturers and learn directly from their competitors.

## Final Thoughts

I started this project to identify the countries where people felt mostly positive or negative towards the Pfizer/BioNtech vaccine. That way, Pfizer/BioNtech would know which countries to target or avoid. Unfortunately, the sentiment distribution within each country was typically evenly spread out - there is no obvious recommendation that can be made in this regard.

Having performed sentiment analysis and topic modelling, I am somewhat satisfied with the results, as the stories derived from both techniques not only complement each other, but also line up with reality.

COVID-19 is very relevant to everyone and it is very easy to determine if the interpretation from the data makes sense - we just have to cross reference the news, if it adds up then it's all good.

However, in terms of business applications, I was rather disappointed as there wasn't any ground-breaking findings. It made me realize that doing this project on a global scale made it less actionable. When it comes to interventions to speed up vaccination progress, it's more realistic to tackle it from a domestic angle. Every country comes with its own unique sets of problems and regulations, and without considering those, it became very difficult to come up with concrete recommendations.

