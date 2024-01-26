FROM python:3.10-slim-buster

# puts you into a folder or a container on the Docker container Inside container
WORKDIR /backend-flask

# outside container -> Inside container
# contains dependencies to run the app
COPY requirements.txt requirements.txt

# Inside container
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container 
# . means everything in the current directory 
# first period . - /backend-flask(outside continer)
# second period . /backend-flask (inside container)
COPY . .

# Inside container - set env vars
ENV FLASK_ENV=development

# inside container
EXPOSE ${PORT}

#  CMD commands to run in the shell
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]