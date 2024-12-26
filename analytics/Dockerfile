FROM python:3.10-slim-buster

WORKDIR /src

COPY ./app/requirements.txt requirements.txt

ENV DB_USERNAME=myuser
ENV DB_PASSWORD=mypassword

RUN apt update -y

RUN apt install build-essential libpq-dev -y

RUN pip install --upgrade pip setuptools wheel

RUN pip install -r requirements.txt

COPY ./app .

CMD python app.py