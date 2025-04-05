FROM python:3.9

# Set the working directory in the container
WORKDIR /usr/source/app

# Copy the dependencies file to the working directory
COPY requirements.txt ./

# Install any needed packages specified in the requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the content of the local src directory to the working directory
COPY . .

# Run the applicatoin
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
