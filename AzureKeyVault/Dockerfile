# Use an official OpenJDK runtime as a parent image
FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the built JAR file from target directory to /app
COPY target/AzureKeyVault-0.0.1-SNAPSHOT.jar app.jar

# Expose the port your Spring Boot application runs on
EXPOSE 8080

# Run the application with the active profile set via environment variable
CMD ["java", "-jar", "app.jar", "--spring.profiles.active=${SPRING_PROFILES_ACTIVE}"]
