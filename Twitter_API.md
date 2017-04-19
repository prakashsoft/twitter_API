================================================================================
By utilizing the Twitter Streaming API,
create a simple web app that filter tweets from a location specified by the user.

-Elasticsearch for Tweets:
 E1. Setup mapping that indexes a tweets collection
 E2. The coordinates properties will be mapped as the geo point type for use with the geo query
 E3. Seed up to 24 hours of tweets

-Create a continuous tweets consumer task that:
 W1. Consumes the Twitter Public Stream API with location filter, which with coordinates that covers the earth's surface
 W2. Parse the raw JSON
 W3. Run sentiment analysis on the text
 W4. Insert the geo tweets into Elasticsearch

-On a simple single-page web app, the user should be able to:
 U1. Enter the lat/long coordinates with an radius in a form
 U2. See top 250 positively scored tweets within that area, sorted descendingly by time
 U3. Additionally, tweets can be filtered on database with specific keywords (i.e.: #amazing, "red panda", obama, etc)

Requirements:
- Git/Github, *commit often* with comments
- Deploy functional app, ie: EC2, Heroku, AppEngine (or equivalent)
- Display the search result as a feed

Resources:
=========
https://dev.twitter.com/streaming/reference/post/statuses/filter
https://pypi.python.org/pypi/tweepy/
https://textblob.readthedocs.org/en/dev/quickstart.html#sentiment-analysis
https://www.elastic.co/guide/en/elasticsearch/reference/current/geo-shape.html#_circle
https://www.elastic.co/guide/en/elasticsearch/client/python-api/current/index.html
https://www.elastic.co/found/signup


Solution:


