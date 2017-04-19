# twitter_API

================================================================================


Resources:
=========
https://dev.twitter.com/streaming/reference/post/statuses/filter
https://pypi.python.org/pypi/tweepy/
https://textblob.readthedocs.org/en/dev/quickstart.html#sentiment-analysis
https://www.elastic.co/guide/en/elasticsearch/reference/current/geo-shape.html#_circle
https://www.elastic.co/guide/en/elasticsearch/client/python-api/current/index.html
https://www.elastic.co/found/signup


Solution:
============================================
Installation & Setup of elasticsearch and Kibana

Follow the Installation & Setup Guide to install and test the Elastic Stack (you can skip this step if you have a working installation of the Elastic Stack)

## Run Elasticsearch & Kibana

  <path_to_elasticsearch_root_dir>/bin/elasticsearch
  <path_to_kibana_root_dir>/bin/kibana
Check that Elasticsearch and Kibana are up and running.

Open localhost:9200 in web browser -- should return status code 200
Open localhost:5601 in web browser -- should display Kibana UI.

Run Example
==============================
## Configure example to use your Twitter API keys

Get Twitter API keys and Access Tokens

This example uses the Twitter API to monitor Twitter feed in real time. To use this, you will first need to create a Twitter app to get your Twitter API keys and Access Tokens.

## need to modify Logstash config file to use your Twitter API credentials

## ingest data into Elasticsearch using Logstash

Execute the following command to start ingesting tweets of interest into Elasticsearch.

 <path_to_logstash_root_dir>/bin/logstash -f twitter_logstash.conf
Verify that data is successfully indexed into Elasticsearch

Running http://localhost:9200/twitter_elastic_example/_count should show a positive response for count
## Visualize data in Kibana

Access Kibana by going to http://localhost:5601 in a web browser Connect Kibana to the twitter_elastic_example index in Elasticsearch.
Click the Management tab >> Index Patterns tab >> ** Add New. Specify twitter_elastic_example as the index pattern name and click Create to define the index pattern.
Load sample dashboard into Kibana Click the Management tab >> Saved Objects tab >> Import, and select twitter_kibana.json Open dashboard
Click on Dashboard tab and open Sample Twitter Dashboard dashboard. 
