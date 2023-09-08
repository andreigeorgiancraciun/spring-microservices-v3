# Use a lightweight base image with Java 17
FROM openjdk:17-slim

# Set the working directory
WORKDIR /app

# Copy the entrypoint script and application JAR
COPY docker-entrypoint.sh target/naming-server-0.0.1-SNAPSHOT.jar ./

# Make the entrypoint script executable
RUN chmod +x docker-entrypoint.sh

# Expose the application port
EXPOSE 8761

# Specify the entrypoint command
CMD ["./docker-entrypoint.sh"]