## Dockerfile
# Use an official Python runtime as a parent image
FROM python:3.11-alpine  as base

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Make port 5001 available to the world outside this container
EXPOSE 5001

# Define environment variable
ENV CONTAINER_API_URL="https://<endpoint>.cognitiveservices.azure.com"
ENV API_KEY="KEYS"

# Run app.py when the container launches
CMD ["python", "app.py"]