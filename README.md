# REST API Example with EvoMaster

This repository provides an example of a **REST API** with **EvoMaster** configured for automated testing.

## **Project Overview**
- **Framework**: Spring Boot
- **Database**: Embedded H2
- **Requirements**: JDK 8, Maven
- **Testing**: Supports both **White-Box and Black-Box** testing using EvoMaster

A [video tutorial](https://youtu.be/ORxZoYw7LnM) is available on writing an EvoMaster Driver for White-Box Testing.

---

## **Running White-Box Testing**

### **Steps to Run White-Box Testing**
1. **Write an EvoMaster driver** for the API.
2. **Download the EvoMaster JAR** file.
3. **Run EvoMaster** using the command below:

#### **Example Commands**
```sh
# Run for 30 seconds and generate tests
java -jar evomaster.jar --maxTime 30s --outputFolder src/test/java/whitebox_tests

# Run for 1 hour, stopping early if no progress is made in 10 minutes
java -jar evomaster.jar --maxTime 1h --prematureStop 10m --outputFolder src/test/java/whitebox_tests
```

How to start a black box testing:

```declarative
cd Graphql-example

java -jar ../rest-api-example/evomaster.jar  --problemType GRAPHQL --bbTargetUrl http://localhost:4000/graphql --blackBox true --maxTime 30s --ratePerMinute 60 --outputFormat JAVA_JUNIT_4 --outputFolder src/test/java/blackbox_tests
```

## **Running Black-Box Testing**

### **Prerequisites**
Before running Black-Box testing, ensure the following:
- The target API is **running and accessible**.
- You have **downloaded the EvoMaster JAR**.
- The API supports **REST, GraphQL, or RPC**.
- You have the **correct API URL** for testing.

---

### **How to Run Black-Box Testing**
1. **Navigate to the target API directory**
   ```sh
   cd Graphql-example
    ```
2. Run EvoMaster with Black-Box mode enabled
    ```sh
    java -jar ../rest-api-example/evomaster.jar  --problemType GRAPHQL --bbTargetUrl http://localhost:4000/graphql --blackBox true --maxTime 30s --ratePerMinute 60 --outputFormat JAVA_JUNIT_4 --outputFolder src/test/java/blackbox_tests
    ```

