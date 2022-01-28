# lets-sync
This repository contains possible ways to sync mongodb with ElasticSearch and one working example with explanation.

Let it Sync! Using Monstache to sync MongoDb and Elasticsearch in real-time.

Many of us might have heard about elasticsearch. It is an open-source NoSQL search engine that is commonly used to search and analyze data. With that being said, we know that elasticsearch is not recommended to be used as a primary database, hence we always need a database to be used with Elasticsearch and keep them synced!

In order to sync elasticsearch with relational databases, there are tools like JDBC and logstash, and many tutorials and articles on how to integrate that but elasticsearch does not provide the required MongoDB JDBC support, which leaves us with very few tools which can be used to sync MongoDB and elasticsearch:

Mongo Connector:
According to its Github:
“ mongo-connector creates a pipeline from a MongoDB cluster to one or more target systems, such as Solr, Elasticsearch, or another MongoDB cluster. “
But the drawback of Mongo Connector is that it does not have very good support for Elasticsearch 6+. Not to forget that its repository has not been updated for more than a year.


Trasporter:
Transporter is a good tool to export data from MongoDB to elasticsearch, but it does not provide real-time syncing.


Mongoosastic:
According to its Github:
“Mongoosastic is a mongoose plugin that can automatically index
your models into elasticsearch.”
But, it is only useful when changes in MongoDB are done through the server, any changes done directly to MongoDB will not reflect in Elasticsearch


Monstache
Sync MongoDB to Elasticsearch in realtime


Monstache is a sync daemon written in Go that continously indexes your MongoDB collections into Elasticsearch. 
Monstache gives you the ability to use Elasticsearch to do complex searches and aggregations of your MongoDB data and easily build realtime Kibana visualizations and dashboards.

for more details please visit
https://rwynn.github.io/monstache-site/

github: https://github.com/rwynn/monstache
