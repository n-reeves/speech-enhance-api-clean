#start from python base image
FROM python:3.10.16

#set working directory
WORKDIR /code

#add requirements file
COPY ./requirements.txt /code/requirements.txt

#install dependencies
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

# #add contents to path   
# ENV PYTHONPATH "${PYTHONPATH}:/code/app"

# add python code
COPY ./app/ /code/app/

#specify default commands
CMD ["fastapi", "run", "app/main.py", "--port", "80"]

