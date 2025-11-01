FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /workspace

# Copy the pom.xml and source code into the container
COPY pom.xml .
COPY src ./src

# Install Maven
RUN apt-get update && apt-get install -y maven

# Package the application
RUN mvn clean package

# Command to run the application
CMD ["java", "-cp", "target/my-java-workspace-1.0-SNAPSHOT.jar", "com.example.App"]