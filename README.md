# docker-training


WhaleSay
#######
docker run docker/whalesay cowsay you are awesome

#################################
Create the "hello_docker.py" file
#################################
print("Hello, World!")


################################
Create the requirements.txt file
################################

scikit-learn==1.2.0


######################
Create the Docker File
######################
FROM python:3.9

# Set the working directory within the container
WORKDIR /app

# Copy the Python script into the container
COPY dock_test.py .

# Install any dependencies required by your Python script
# For example, if you have a requirements.txt file, you can uncomment the following line
COPY requirements.txt .
RUN pip install -r requirements.txt

# Define the command to run your Python script
CMD ["python", "hello_docker.py"]




################
Create the Image
################

docker build -t helloimage:latest .




####################
Create the Container
####################

docker run --name hellocontainer helloimage:latest

Docker mini-training course for the SP23 DS460 class.


