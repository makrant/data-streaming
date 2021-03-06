
# Kafka - Spark Streaming Example

1. Start Kafka tweet producer to write to a topic (https://github.com/rbotla/data-streaming/tree/master/kafka/producer-consumer/python)
2. Run the following command for Spark streaming to get the tweets from Kafka and process the tweets in real-time

Ensure to update an appropriate "2.11:2.4.5" version in the follownig command. Check ```ls $SPARK_HOME/jars``` to see the version associated with the kafka jars. Note there is a ":" in the before the Spark version.

This program accepts three arguments - Kafka Server, Port and the topic name from where tweets to be retrieved.
```
cd /spark-streaming/kafka
spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.4.5 kafka_twitter.py localhost 9092 covid
```
Reference - https://spark.apache.org/docs/latest/structured-streaming-kafka-integration.html
