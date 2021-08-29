# set base image
FROM python:3.8

# set a key-value label for the Docker image
LABEL maintainer="Debarghya Dey"

# copy files from the current directory to the  `/app` directory in the container
COPY . /app

#  defines the working directory within the container
WORKDIR /app

# run commands to upgrade pip and install dependencies defined in the requirements.txt file and initialise the database with `init_db.py` 
RUN python -m pip install --upgrade pip && pip install -r requirements.txt && python3 init_db.py

# exposes the container port
EXPOSE 3111

# start the `app.py` application.
CMD [ "python3", "app.py"  ]
