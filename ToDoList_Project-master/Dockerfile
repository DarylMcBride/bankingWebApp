FROM maven:latest as maven
COPY . /build
WORKDIR /build
FROM java:8
WORKDIR /opt/back-end
COPY --from=maven /build/target/IndividualProject-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["/usr/bin/java", "-jar", "app.jar"]
