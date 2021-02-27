# kafka

## Local setup

```
# install kafka 
brew install kafka

# start zookeeper 
zookeeper-server-start /usr/local/etc/kafka/zookeeper.properties

# start kafka server
kafka-server-start /usr/local/etc/kafka/server.properties

# create kafka topic
kafka-topics --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

# initialize producer console
kafka-console-producer --broker-list localhost:9092 --topic test

# initialize consumer console
kafka-console-consumer --bootstrap-server localhost:9092 --topic test
--from-beginning
