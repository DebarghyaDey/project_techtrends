# set base image
FROM python:3.8

# set a key-value label for the Docker image
LABEL maintainer="Debarghya Dey"

# copy files from the current directory to the  `/app` directory in the container
COPY . /app

#  defines the working directory within the container
WORKDIR /app

# run commands install dependencies defined in the requirements.txt file 
RUN  pip install -r requirements.txt 

# exposes the container port
EXPOSE 3111

#start.sh is the bash file which will execute init_db.py and app.py
RUN chmod +x ./start.sh

# start the `start.sh` file.
CMD ["./start.sh"]
