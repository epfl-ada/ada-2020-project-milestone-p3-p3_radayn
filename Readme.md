# Socio-emotional interactions on Twitter #

**Team Name: RadaYN**

**Team Member: Rachel Lee, Nouha Kacimi, Yuqi Wang**

### Abstract ###
In this digital age, social interactions have transcended the physical sphere to the virtual one. Encouraging this phenomenon are social media platforms such as Twitter. One is able to easily interact with others or spread content by retweeting a tweet. Inspired by how much influence and interaction people can have on social media, our team has decided to further explore the concept of homophily presented in the paper “Testing Propositions Derived from Twitter Studies” by studying the socio-emotional division between Twitter users. This will be done by a sentiment analysis which evaluates the nature of tweets and hashtags - positive, neutral or negative. The polarity of the sentiments of shared content is then studied as a whole of the platform, each user as well as the each users’ followees. Overall, we wish to understand if people have a tendency to interact with others of similar polarity of sentiments.
### Research questions ###
1. Do people have a tendency to share positive or negative content?
2. Is each user generally positive, negative or neutral? 
3. Do users tend to follow users that share similar nature of content?
### Proposed datasets ###
- [Replication dataset](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/L1MJZ6) from the paper. This dataset gives us a list of user IDs, the network of these users and the timeline of users. We will enrich the dataset by using [twitter API](https://developer.twitter.com/en/docs/twitter-api) to get the contents of each tweet and apply sentiment analysis.
- Before we actually dive into the analysis, we will verify if sentiment analysis can be done on the proposed dataset. If not, we will get new user IDs and generate our own dataset by checking the recent tweets on twitter.
### Methods ###
- **Data Collection**: In our research, obtaining the contents of tweets is the foundation. Twitter has an official API which we can utilize to get required dataset. We can use the [tweepy](https://www.tweepy.org/) python package for accessing official API and obtain contents of tweets for each user ID in the proposed dataset.
- **Preprocessing**: We will select those who have at least 100 (the number can change) tweets and reconstruct our network of users. Then we will do basic data cleaning on text data (contents). 
- **Sentiment Analysis**: To apply sentiment analysis, we will use NLP techniques. There are several candidate python packages: [TextBlob](https://textblob.readthedocs.io/en/dev/), [NLTK](https://www.nltk.org/), and etc. Sentiment analysis will be carried on the dataset to verify if one specific tweet is positive or negative or neutral. We will also verify if one user is positive or negative by analyzing all his tweets and label them with a score. To answer question 1 and 2, we will evaluate the polarity (positive or negative or neutral) of each tweet and label them with a polarity score. Then, we will calculate the number of positive or negative tweets for each user (or calculate his/her average polarity score) and label this user with a score. These data will be helpful to test our proposition. To answer question 3, we will analyze the main polarity of the followees of each user of known polarity by calculating the number of positive, negative and neutral followers.
### Proposed timeline ###
- **By 4 December**: Check if the IDs are active and generate new ones otherwise. Collect contents of tweets dataset.
- **By 11 December**: Preprocess the dataset, select valid users with at least a number of tweets. Conduct sentiment analysis.
- **By 18 December**: Write the report and make the video to show the results and do the individual part (replication of the figure).
### Organiztion within the team ###
![](https://github.com/epfl-ada/ada-2020-project-milestone-p3-p3_radayn/blob/master/organization.PNG?raw=True)