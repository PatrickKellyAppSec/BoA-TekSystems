# Use a minimal base image
FROM alpine:3.18

# Add a non-root user and group
RUN addgroup -S appgroup && adduser -S appuser -G appgroup

# Install only necessary packages
RUN apk --no-cache add curl

# Switch to the non-root user
USER appuser

# Set the working directory
WORKDIR /home/appuser

# Copy the application code
COPY . .

# Command to run the application
CMD ["sh", "-c", "echo 'Hello, secure world!'"]
