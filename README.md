# SMACK_Tweets

Its a small application which collects tweets from twitter and process it with spark streaming and ingest it in cassandra ring.
To run the application you need to do following steps. <br />

1. First we need to start kafka server to ingest tweets in 'tweets' topic.

> bin/zookeeper-server-start.sh config/zookeeper.properties

> bin/kafka-server-start.sh config/server.properties

2. Now we need to start cassandra for ingesting tweets

>bin/cassandra -f

3. Simply start kafka producer to collect tweets

>sbt run

4. Simply start the spark streaming job to consume tweets from kafka queue and process it.

>sbt run
