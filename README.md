# WeRateDogs Twitter Data Wrangling and Exploration
## by Morufdeen Olatunbosun Atilola


## Introduction

We are performing Data Wrangling on the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comments about the dog.

This data have some quality and tidiness issues that needs to be identified and clean by following the data wrangling process for the data to be fit for analysis. 

At the end of the project:
1. Identify at least 8 quality issues and 3 tidiness issues
2. Clean the identified issues
3. Perform some analysis and bring out at least 3 insights and 1 visualization from the cleaned data. 

### Gathering Data 

The first step of data wrangling is to gather the required data to be cleaned. This involves collating the data from different sources either manually or programmatically.

For this project, we used 3 separate data, each of which was gathered separately.

1. **Twitter_archive_enhanced data**: This data was downloaded manually, upload to the project workspace, and read into pandas DataFrame.
2. **The tweet image_predictions**: This data was gathered programmatically by using the Request library and the given URL. It is a .tsv file. It was downloaded programmatically into the workspace and read into pandas DataFrame with tabular separation (\t)
3. **Tweet_json data**: This required querying Twitter API data using the Tweepy library and stored in tweet_json.txt.
> I used the provided `twitter_api.py` code and `tweet_json.txt` due to my inability to secure access to the Twitter API data after waiting for a day. So, I used the provided one and I opened and read the JSON text file to extract the needed column (tweet_id, favorite_count, and retweet count) to be stored in a pandas dataframe called `tweet_json_df`

### Cleaning Data

I performed cleaning following the established way of cleaning identified issues by defining, coding, and testing. Each of the issues was properly addressed with defined cleaning methods and properly tested.

After cleaning all the quality and tidiness issues, the 3 datasets was merged and stored in `twittwe_archive_master` in a CSV file. This master data was later used for analysis and visualization.


### Insights:

1. According to the predictions analysis, it was found that golden_retriever is the most popular breed with 139 samples majority of which received ratings of 12/10 (54 out of 139), only 2 of the golden_retriever received rating of 14/10

2. The dogs with the highest rating 15/10 was predicted not to be dog. For this reason, it has 0 favorite count and 38 retweet count

3. There is a strong correction between the favorite count and retweet count (0.91). However there is a weak correction (0.3 and 0.4) between these counts and the dog rating