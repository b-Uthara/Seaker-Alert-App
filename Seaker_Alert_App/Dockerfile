# Use an official Python runtime as a parent image
FROM python:3.11-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Set Flask environment to production (disable debug mode)
ENV FLASK_ENV=production


# Expose port 80 for the app
EXPOSE 80


# Define the default command to run the Python application with Gunicorn
CMD ["gunicorn", "-w","4" ,"-b", "0.0.0.0:5000", "Seaker-Alert-App.Alert_System:app"]