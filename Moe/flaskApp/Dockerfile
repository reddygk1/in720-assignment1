FROM python:2.7
MAINTAINER Gowtham Reddy <reddygk1@student.op.ac.nz>
ENV REFRESHED_AT 2016-09-06

ADD . /flaskApp
WORKDIR /flaskApp

RUN pip install -r requirements.txt

RUN uwsgi --build-plugin https://github.com/unbit/uwsgi-consul

ENTRYPOINT [ "uwsgi", "--ini", "uwsgi-consul.ini", "--ini", "uwsgi-consul.ini:server1"]

CMD []


