# Use the official Ubuntu image
FROM ubuntu:latest

# Set the working directory inside the container
WORKDIR /app

# Copy necessary files into the container
COPY requirements.txt /app/
COPY devops /app/devops/

# Install Python and pip, and install required packages
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip3 install --no-cache-dir -r requirements.txt && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set the default command to run the app
CMD ["python3", "devops/manage.py", "runserver", "0.0.0.0:8000"]




