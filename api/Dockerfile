FROM python:3.8-buster

RUN groupadd -r HNG && useradd -r -g HNG HNG

RUN chsh -s /usr/sbin/nologin root

WORKDIR /usr/api

COPY requirements.txt requirements.txt 
RUN pip install --upgrade pip && pip install -r requirements.txt

COPY . .


CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]

# FROM python:3.8-slim-buster

# RUN apt-get update \
#     && apt-get -y install libpq-dev gcc \
#     && pip install psycopg

# WORKDIR /app

# COPY requirements.txt requirements.txt
# RUN pip3 install -r requirements.txt

# COPY . .

# EXPOSE 8000

# CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]