Basic Kafka Command line statements

Download and install Kafka. 
Under the >bin directory

1) Start zookeeper
bin/zookeeper-server-start.sh config/zookeeper.properties

2) Create new topic
bin/kafka-topics.sh --zookeeper localhost:2181 --create --topic kafka_topic --partitions 2 --replication-factor 1

3) Start kafka server
bin/kafka-server-start.sh config/server.properties

4) start kafka producer
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic kafka_topic

5) Start kafka consumer
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic kafka_topic

6) Describe topic 
bin/kafka-topics.sh --zookeeper localhost:2181 --describe --topic kafka_topic
