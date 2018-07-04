event-ingestion-router
=======================

Built with Java 8+, Apache Camel (2.22.0) and Spring Boot (2.0.3.RELEASE)

Tested with JUnit (4.11)

Execution
* Spring-boot, assumes ActiveMQ is running locally
* Docker (w/ Compose) - also starts up ActiveMQ and Hawtio

Both require building the project first

`mvn clean install`

### Docker Execution

Start Docker

`docker-compose up`

View ActiveMQ (_admin/admin_)

`http://localhost:8161/admin/`

View Spring-Boot App

`http://localhost:9001/actuator/info`

View Hawtio

`http://localhost:8090/hawtio/welcome`


### Spring-Boot Execution

Executes with Spring Boot

`mvn spring-boot:run -Drun.arguments="-Xmx256m,-Xms128m"`

Runs against ActiveMQ (5.14.0) using JMeter (2.13); requires activemq-all-5.14.0.jar in lib directory

>Message content can viewed in the ActiveMQ or hawtio Web Consoles.

Navigate to http://localhost:8161/admin/

OR 

launch hawtio

    $java -jar hawtio-app.jar --port 8090 

and navigate to http://localhost:8090/hawtio/welcome   
