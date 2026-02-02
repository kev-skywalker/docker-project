FROM python:3.13-slim
LABEL maintainer="kevinnkouimi@gmail.com"
COPY  student_age.py requirements.txt /
RUN apt-get update && apt-get install -y \
    gcc \
    libldap2-dev \
    libsasl2-dev \
    libssl-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
RUN pip install --upgrade pip
RUN pip3 install -r /requirements.txt
VOLUME ["/data"]
EXPOSE 5000
CMD [ "python3", "./student_age.py" ]
