# Kafka Producer and Consumer in Python

![Kafka Twitter](kafka-consumer-twitter.png)

Instructions to install Python3.x on Debian 9
```
sudo apt update
sudo apt install python3-pip
pip3 --version
```

Install required libraries
```
pip3 install kafka
pip3 install kafka-python
pip3 install python-twitter
pip3 install tweepy
pip3 install configparser
```

Create a Kafka topic called covid
```
kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 3 --topic covid
```

```
cd kafka/consumer-producer/python
```
Update your Twitter developer app credentials in config.cfg file. Refer to https://themepacific.com/how-to-generate-api-key-consumer-token-access-key-for-twitter-oauth/994/

Run the twitter kafka producer program
```
python3 twitter_producer.py
```