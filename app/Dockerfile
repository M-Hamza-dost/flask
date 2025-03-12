FROM python:3.11-alpine
WORKDIR /app

RUN apk add mysql mysql-client gcc mariadb-connector-c-dev musl-dev

COPY ./requirments.txt /app/requirments.txt

RUN pip install -r requirments.txt

RUN pip install requests

COPY . /app

CMD [ "python", "prod_app.py"]
