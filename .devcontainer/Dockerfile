# The original image can be any Python version according to your usage.
FROM python:3.7.17-slim-buster

# Specifies the working directory in the container. This can also be changed as desired.
# However, it must match the destination directory name specified in the following COPY command.
WORKDIR /app

RUN apt update
RUN apt install nodejs npm -y
RUN npm install -g azure-functions-core-tools@3 --unsafe-perm true

# Copy the requirements.txt and run pip install.
COPY ./requirements.txt /app
RUN pip install -r requirements.txt

