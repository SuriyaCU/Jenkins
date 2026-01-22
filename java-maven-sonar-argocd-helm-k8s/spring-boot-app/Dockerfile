FROM adoptopenjdk/openjdk11:alpine-jre

# Install docker CLI, bash, curl
RUN apk add --no-cache docker bash curl git

# Install Maven
RUN apk add --no-cache maven

# Copy your artifact
ARG artifact=target/spring-boot-web.jar
WORKDIR /opt/app
COPY ${artifact} app.jar

ENTRYPOINT ["java","-jar","app.jar"]
