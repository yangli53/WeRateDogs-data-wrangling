# WeRateDogs-data-wrangling

The dataset that I wrangled is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account 
that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators are 
almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers 
and has received international media coverage.

In this project, I first gathered data from three sources:

1. The WeRateDogs Twitter archive. I downloaded **twitter_archive_enhanced.csv** directly and read it in Python as `twitter`.
2. The tweet image predictions. I downloaded **image_predictions.tsv** programmatically using the Requests and read it as `image`.
3. Each tweet's retweet count and favorite count. I used tweet IDs from **twitter_archive_enhanced.csv**, queried the Twitter API for each 
tweet's JSON data using Tweepy and stored JSON data in **tweet_json.txt**. Then I read this file line by line into a pandas DataFrame with 
tweet ID, retweet count, and favorite count as `tweet`.

Then I assessed the data visually and programmatically to identify at least 8 quality issues and 2 tidiness issues.

Then I cleaned the data accordingly and stored it in file named **twitter_archive_master.csv** and in a SQLite database.

Finally, I analyzed the data and visualized my findings in **act_report.html**. My wrangling process was coded in **wrangle_act.ipynb** and
reported in **wrangle_report.html**.
