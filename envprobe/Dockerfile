FROM alpine:3.19

# Create the working directory
WORKDIR /app

# Copy the startup script into the working directory
COPY envprobe/startup-script.sh /app

#installing curl
RUN apk add --no-cache curl ca-certificates

# Create a non-root user to run the script
RUN adduser -D nonrootuser

# Ensure the script is executable
RUN chmod 755 startup-script.sh

# Set the default environment variable
ENV APP_ENV=dev

# Switch to the non-root user for runtime
USER nonrootuser

# Run the startup script as the container entrypoint
ENTRYPOINT [ "./startup-script.sh" ]
