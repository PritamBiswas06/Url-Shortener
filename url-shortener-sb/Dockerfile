# Use a Maven image for building
FROM maven:3.9.4-eclipse-temurin-17 AS build

WORKDIR /app

# Copy Maven wrapper files first
COPY mvnw ./ 
COPY .mvn/ .mvn/ 

# Give execution permissions to Maven wrapper
RUN chmod +x mvnw

# Copy the pom.xml and download dependencies
COPY pom.xml . 
RUN ./mvnw dependency:go-offline

# Copy the source code
COPY src/ src/

# Build the application (skipping tests)
RUN ./mvnw clean package -DskipTests

# Use a runtime-only image (smaller)
FROM eclipse-temurin:17-jre

WORKDIR /app

# Copy the built JAR file
COPY --from=build /app/target/url-shortener-sb-0.0.1-SNAPSHOT.jar /app/app.jar

# Expose the application port
EXPOSE 8080

# Run the application
ENTRYPOINT ["java", "-jar", "/app/app.jar"]
