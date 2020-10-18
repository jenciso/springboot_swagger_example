# Rest Service Documentation using Swagger

## Getting Started

Build the artifact

```shell
mvn package
```

Test

```shell
java -jar target/spring-boot-web-0.0.1-SNAPSHOT.jar
```

Create a Dockerfile

```Dockerfile
FROM openjdk:alpine
COPY target/spring-boot-web-0.0.1-SNAPSHOT.jar /
ENTRYPOINT ["java", "-jar", "/spring-boot-web-0.0.1-SNAPSHOT.jar"]
```

Build the image

```shell
docker build . -t spring-boot-web:0.0.1
```

Run it

```shell
docker run -p 8080:8080 --rm spring-boot-web:0.0.1:latest
```
