# KafkaTest
Kafka + Intellij IDEA + Maven

Requirements: 
- Java JDK 8 +
- Intellij IDEA
- Maven

# Open intelliJ and select import project and select the pom.xml file

mvn clean compile exec:java -Dexec.mainClass="io.grandino.kafka.example.javaspringkafkaexample.JavaSpringKafkaSimpleProducer" -Dexec.args="test"

mvn clean compile exec:java -Dexec.mainClass="io.grandino.kafka.example.javaspringkafkaexample.JavaSpringKafkaSimpleConsumer" -Dexec.args="test"

Was used the Spring Initilzr web
- access the website and generate the project package (https://start.spring.io)
- added the WEB and Kafka dependency
- project MAVEN
