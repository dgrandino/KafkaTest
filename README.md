# KafkaTest
Kafka + Intellij IDEA + Maven

Requirements: 
- Java JDK 8 +
- Intellij IDEA
- Maven

# Create a Kafka cluster 
-Download binary .tgz Kafka (https://kafka.apache.org/downloads)
-Extract with 7zip 
-From the kafka installation folder run the following command lines:
  - .\bin\windows\zookeeper-server-start.bat config\zookeeper.properties
  - .\bin\windows\kafka-server-start.bat config\server.properties
  - Create a Topic: .\bin\windows\kafka-topics.bat --create --boostrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test
Created topic test
  - Once created, run the following command lines from two windows:
    - .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic teste --from-beginning
    - .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic test
-What is written in the producer will be shown in the consumer  

# Open intelliJ and select import project and select the pom.xml file

- run the following command lines in different windows to simulate producer o and consumer
 - mvn clean compile exec:java -Dexec.mainClass="io.grandino.kafka.example.javaspringkafkaexample.JavaSpringKafkaSimpleProducer" -Dexec.args="test"
 - mvn clean compile exec:java -Dexec.mainClass="io.grandino.kafka.example.javaspringkafkaexample.JavaSpringKafkaSimpleConsumer" -Dexec.args="test"

-What is written in the producer will be shown in the consumer  

Was used the Spring Initilzr web
- access the website and generate the project package (https://start.spring.io)
- added the WEB and Kafka dependency
- project MAVEN
