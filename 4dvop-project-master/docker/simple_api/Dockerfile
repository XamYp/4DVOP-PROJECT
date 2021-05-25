FROM python:3.6.2-stretch

LABEL maintainer="maxence.xxxxx@supinfo.com"

COPY student_age.py /

RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv

RUN mkdir /data
COPY student_age.json /data
VOLUME /data

EXPOSE 5000

CMD ["python", "./student_age.py"]
