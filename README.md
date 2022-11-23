
# Data Wrangling and Analysis
## Project Overview
WeRateDogs is a Twitter account that rates people's dogs with a humorous commen about the dog.
## The project involves the following steps:
In this section three different data are collected.
**Step 1: Gathering data**
> - twitter-archive-enhanced.csv, given file
> - image-predictions.tsv
> - tweet-json.txt, is collected using weepy API based on the ID from the `twitter-archive-enhanced.csv`

**Step 2: Assessing data**
> **Summery of the Assessment** 

Quality issue

**Twitter-archive-enhanced table**
> - missing value in reply_to_status_id
> - missing value in reply_to_user_id
> - missing value in retweeted_status_id
> - misiing value in retweeted_status_id
> - missing value in retweeted_status_timestamp
> - missing value in the expanded_url
> - use only original tweets, remove the rows with retweet and replay
> - size of the reocrd in the image prediction should be 2356 instade of 2074
> - timesatmp: its datatype should be datetime instead of object.
> - tweet_id: its datatype should be object.
> - name: the value of name column, instead of a replace with valid name and should start with capital later
> - rating_numenator with floating value are not correctly extracted (in correct)
> - the source value is invalid data/inaccurate and needs to remove all the unneccessay symbols and characters
> - the text value is invalid/inaccurate and needs remove the special characters and numbers and symbols
> - some of the vlaue of columns doggo, floofer, pupper, puppo is None instead of NaN, should be replaced

**Tweet_df table**
> - the id column name should be renamed with tweet_id for consisstency with the other datasets

**image-predictions table**
> - the Value in each prediction is inconsistent, some of them satrt with either capital or small letter.
> - duplicated jpg_url, duplication should be handled
> - the name of each prediction are not clearly understandable, should be changed
**Tidiness**:
> - archive_df: the columns doggo', 'floofer', 'pupper', 'puppo' describe dog satge, it needs to be structured
> - the three tables should be merged to create the master data using the tweet_id

**Step 3: Cleaning data**
- in this section all the above adentified problems got handled in a way appropriate to use for analysis. the solution was defind in a format of
> - define: defining the problem and its way to solve
> - code: the actual code to do
> - test: tesing its correctness
> - for more detailed inforamtion click [here](wrangle_act.ipynb)

**Step 4: Storing data**
- in this section the preprocessed data has stored in master file and database

**Step 5: Analyzing, and visualizing data**
- seven critical questions has been included to perform analysing and get insight about the dataset

**Step 6: Reporting**
- reporting has made as ususal
