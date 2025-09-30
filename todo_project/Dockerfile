# Use Python base image
FROM python:3.11-slim

# Set working directory
WORKDIR /app
 
# Copy requirements and install
# COPY requirements.txt .
# RUN pip install --no-cache-dir -r requirements.txt
COPY todo_project/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
# Copy project files
COPY . .

# Expose Django port
EXPOSE 8000

# Run server 
CMD ["gunicorn", "todo_project.wsgi:application", "--bind", "0.0.0.0:8000"]

