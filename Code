import os
import tweepy as tw
import pandas as pd
import csv

# Fill the X's with the credentials obtained by 
# following the above mentioned procedure. 
consumer_key = "xxx"
consumer_secret = "xxx"
access_token = "xxx"
access_token_secret = "xxx"

auth = tw.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)
api = tw.API(auth, wait_on_rate_limit=True)

#Write tweets to a CSV File


csvFile = open('result3.csv', "a")
csvWriter = csv.writer(csvFile)


#Searches for tweets with hashtag
#earch_words = "#Paytm"
#ate_since = "2011-10-10"

#Avoids Retweets, searches for text in  Tweets
new_search = "Payment + Wallet -filter:retweets"
for tweet in tw.Cursor(api.search,
                       q=new_search,
                       lang="en",
                       since=date_since).items(9999):
                       csvWriter.writerow([tweet.user.screen_name, tweet.text])
csvFile.close()

csvFile = open('result3.csv', "a")
csvWriter = csv.writer(csvFile)
