# Use official Python 3.10 image as the base
FROM python:3.10

# Set the working directory
WORKDIR /app

# Copy the requirements file and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Django project files
COPY . .

# Expose the port Django runs on
EXPOSE 8000

# Run migrations and start Django server
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "smartquest.wsgi:application"]
