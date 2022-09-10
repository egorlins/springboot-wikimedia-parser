# Kafka
Kafka download

https://kafka.apache.org/quickstart

Kafka Run zookeeper (separate CMD)

.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

Kafka run server (separate CMD)

.\bin\windows\kafka-server-start.bat .\config\server.properties

Create topic (any CMD)

.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

Kafka send events for topic quickstart-events (separate CMD)

.\bin\windows\kafka-console-producer.bat --topic quickstart-events --bootstrap-server localhost:9092

Kafka get events for topic quickstart-events (separate CMD)

.\bin\windows\kafka-console-consumer.bat --topic quickstart-events --from-beginning --bootstrap-server localhost:9092

###

Create Spring project

https://start.spring.io/

Spring Kafka documentation

https://docs.spring.io/spring-kafka/reference/html/#quick-tour

Wikimedia stream

https://stream.wikimedia.org/v2/stream/recentchange

OkHttp EventSource

https://mvnrepository.com/artifact/com.launchdarkly/okhttp-eventsource

this also be needed https://mvnrepository.com/artifact/com.squareup.okhttp3/okhttp

Jackson Core

https://mvnrepository.com/artifact/com.fasterxml.jackson.core/jackson-core

Jackson Databind

https://mvnrepository.com/artifact/com.fasterxml.jackson.core/jackson-databind

Database

create database wikimedia;


# run/test
mvn clean install

and see:

[INFO] springboot-wikimedia-parser ........................ SUCCESS [  1.284 s]

[INFO] kafka-producer-wikimedia ........................... SUCCESS [  3.581 s]

[INFO] kafka-consumer-db .................................. SUCCESS [  1.295 s]

can be seen from commandline

.\bin\windows\kafka-console-consumer.bat --topic wikimedia-recent_change --from-beginning --bootstrap-server localhost:9092