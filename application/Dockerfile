FROM python:alpine3.16

# Set the working directory to /app
WORKDIR /app

# Copy the source contents into the container at /app
COPY app.py mongo.py requirements.txt static/ templates/ /app/
COPY /static/ /app/static
COPY /templates /app/templates


# Install any needed packages specified in requirements.txt
RUN pip install -r requirements.txt

# Make port 5000 available to the world outside this container
EXPOSE 5000


# Run app.py when the container launches
ENTRYPOINT [ "python", "app.py"]
