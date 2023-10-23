# Stage 1: Build the application
FROM python:3.8-slim-buster as builder

# Set the working directory
WORKDIR /app

# Copy only the necessary files for the build
COPY calc.py /app/

# Stage 2: Create the final minimal image
FROM python:3.8-slim-buster

# Set the working directory
WORKDIR /app

# Copy the application from the builder stage
COPY --from=builder /app /app

# Run the Python script when the container launches
Entrypoint ["Python"]
CMD [ "calculator.py"]

