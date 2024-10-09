# Dockerfile for book-catalog microservice
# Use an official Python runtime as a parent image
FROM --platform=linux/amd64 python:3.8-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY ./app /app

# Install any needed packages specified in requirements.txt
RUN pip install -r requirements.txt

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Define environment variable
ENV DATABASE_URL postgresql://task7project_697a_user:5p0Ns3xocU48iXPPwYsvQgSUUneiB2mv@dpg-cs34gj68ii6s738fqa1g-a.oregon-postgres.render.com/task7project_697a

# Run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]