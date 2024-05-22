FROM busybox

# Work directory inside the container is /app
WORKDIR /app

# Copy the init.sh script into the container
COPY init.sh ./

# Give executable permission to init.sh
RUN chmod +x ./init.sh

# Create data directory for placing files if DATA_PATH is set to /app/data
# Remove this if your DATA_PATH will be set differently
RUN mkdir -p /app/data

# Set necessary environment variables if they are fixed (not recommended for secrets)
# It's better to use Docker secrets or runtime environment variables for sensitive data
# ENV DATA_PATH /app/data
# ENV PG_PASSWORD secret_password
# ENV PG_USERNAME secret_username

# ENTRYPOINT or CMD to run your init.sh could be here if you want it to run by default
# ENTRYPOINT ["./init.sh"]
# Or if you want to pass arguments use CMD
CMD ["./init.sh"]
