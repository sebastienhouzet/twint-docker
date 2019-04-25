# How to use

## Elasticsearch and Kibana

Start to up elaticsearch and kibana
docker-compose up -d

## Execute Twint command

docker-compose run -v $PWD/twint:/srv/twint twint {{CMD TWINT}}

## Examples of command

A few simple examples to help you understand the basics:

``` bash
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username - Scrape all the Tweets from user's timeline.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username -s pineapple - Scrape all Tweets from the user's timeline containing pineapple.
docker-compose run -v $PWD/twint:/srv/twint twint twint -s pineapple - Collect every Tweet containing pineapple from everyone's Tweets.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --year 2014 - Collect Tweets that were tweeted before 2014.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --since 2015-12-20 - Collect Tweets that were tweeted since 2015-12-20.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username -o file.txt - Scrape Tweets and save to file.txt.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username -o file.csv --csv - Scrape Tweets and save as a csv file.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --email --phone - Show Tweets that might have phone numbers or email addresses.
docker-compose run -v $PWD/twint:/srv/twint twint twint -s "Donald Trump" --verified - Display Tweets by verified users that Tweeted about Donald Trump.
docker-compose run -v $PWD/twint:/srv/twint twint twint -g="48.880048,2.385939,1km" -o file.csv --csv - Scrape Tweets from a radius of 1km around a place in Paris and export them docker-compose run -v $PWD/twint:/srv/twint twint to a csv file.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username -es localhost:9200 - Output Tweets to Elasticsearch
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username -o file.json --json - Scrape Tweets and save as a json file.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --database tweets.db - Save Tweets to a SQLite database.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --followers - Scrape a Twitter user's followers.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --following - Scrape who a Twitter user follows.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --favorites - Collect all the Tweets a user has favorited.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --following --user-full - Collect full user information a person follows
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --profile-full - Use a slow, but effective method to gather Tweets from a user's profile (Gathers ~3200 Tweets, docker-compose run -v $PWD/twint:/srv/twint twint Including Retweets).
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --retweets - Use a quick method to gather the last 900 Tweets (that includes retweets) from a user's profile.
docker-compose run -v $PWD/twint:/srv/twint twint twint -u username --resume 10940389583058 - Resume a search starting from the specified Tweet ID.
```

## Datas

For datas generate by twint, you can found result on folder twint

Let's play now :)