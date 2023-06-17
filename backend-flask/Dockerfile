FROM python:3.10-slim-buster

# Set Container Internal Working Directory
WORKDIR /backend-flask

# Copy requirements.txt to working directory
COPY requirements.txt .

# Install Python dependencies
RUN pip3 install --no-cache-dir -r requirements.txt

# Copy the entire project to the working directory
COPY . .

# Set Environment variable
ENV FLASK_ENV=development

# Expose the desired port
EXPOSE 4567

# Run the Flask application
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=4567"]
