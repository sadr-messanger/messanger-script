FROM golang

WORKDIR /app

RUN apt update -y && apt upgrade -y
RUN apt install -y python3-pip
RUN apt install -y python3-dev
RUN apt install -y git

RUN git clone https://github.com/matrix-org/rageshake.git

COPY ./logger/email_body.tmpl /app/rageshake
COPY ./logger/issue_body.tmpl /app/rageshake
COPY ./logger/rageshake.yaml /app/rageshake

RUN cd rageshake && go build