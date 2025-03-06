# rest-api-example
An example of REST API with EvoMaster configured for it.

It requires JDK 8, and Maven.

The API is written with SpringBoot, and uses an H2 embedded database.


A [video](https://youtu.be/ORxZoYw7LnM) 
is available showing how to write an EvoMaster Driver for White-Box Testing. 

How to start:
1. Write a driver
2. add a evomaster.jar
3. start
```declarative
java -jar evomaster.jar --maxTime 20s  --outoutFolder src/test/java 
```