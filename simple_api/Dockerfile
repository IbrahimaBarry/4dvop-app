FROM python:2.7-stretch
LABEL maintainer="Ibrahima BARRY <285748@supinfo.com>"
COPY student_age.py .
RUN apt-get update -y
RUN apt-get install -y python3-dev python3-pip libsasl2-dev libldap2-dev libssl-dev
RUN pip3 install flask flask_httpauth flask_simpleldap python-dotenv
RUN mkdir /data
COPY student_age.json /data
VOLUME /data
EXPOSE 5000
CMD [ "python3", "./student_age.py" ]