# Use the latest Ubuntu image as the base
FROM ubuntu:latest

# Update APT package lists
RUN apt-get update

# Upgrade installed packages
RUN apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix for "externally managed" error if it occurs
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Install Flask-Cors using pip3
RUN pip3 install flask-cors

# Set the working directory
WORKDIR /app

# Copy the Flask application file
COPY ./api.py /app/api.py

# Command to run the Flask server
CMD ["python3", "api.py"]

