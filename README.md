# Spring Boot Wikimedia Kafka DB Integration
+ A Spring Boot project showcasing real-world usage of Spring Boot and Apache Kafka.
+ Implements a Kafka producer to fetch real-time stream data from Wikimedia.
+ Demonstrates efficient transmission of data to a Kafka broker.
+ Utilizes a Kafka consumer to store data into a database.

## Steps to Setup

**1. Download and Install Kafka**

Visit the Apache [Kafka download page](https://kafka.apache.org/downloads) to download the latest version of Kafka and extract it

**2. Start the ZooKeeper server**

Open a terminal and navigate to the Kafka directory.
```bash
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

**3. Start the Kafka server**

In a new terminal window, start the Kafka server:
```bash
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

**4. Clone the Application**

```bash
git clone https://github.com/attrayadas/springboot-wikimedia-kafka-db-integration
```

**5. Create MySQL Database**
```bash
create database wikimedia_db;
```

**6. Change MySQL username and password as per your installation**
+ open `kafka-consumer-database/src/main/resources/application.properties`
+ change `spring.datasource.username` and `spring.datasource.password` as per your MySQL installation

**7. Run Kafka Producer**

Navigate to the `kafka-producer-wikimedia` directory and run the Kafka producer application
```bash
mvn spring-boot:run
```

**8. Run Kafka Consumer**

Navigate to the `kafka-consumer-database` directory and run the Kafka consumer application:
```bash
mvn spring-boot:run
```
