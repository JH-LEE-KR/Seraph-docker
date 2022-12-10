# Dockerfile
# Set base image 
FROM python:3.8
ENV PYTHONUNBUFFERED 1
# Set maintainer
MAINTAINER "Jaeho Lee <dlwogh9344@khu.ac.kr>"

# Get source from github
# RUN apt-get update && apt-get upgrade -y
# Install git
# RUN apt-get install git -y

RUN mkdir /srv/docker-server
ADD . /srv/docker-server

WORKDIR /srv/docker-server

# Install packages
RUN pip install --upgrade pip && pip install -r requirements.txt

# Run django application on the port 8080
# EXPOSE 8080

# Run the django application
# CMD ["bash", "-c", "python manage.py collectstatic --settings=BACKEND.settings.deploy --no-input && python manage.py makemigrations && python manage.py migrate && python manage.py runserver 0.0.0.0:8080"]
# ENTRYPOINT ["bash", "-c", "python manage.py makemigrations && python manage.py migrate"]