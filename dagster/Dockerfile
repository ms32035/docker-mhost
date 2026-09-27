FROM python:3.14-slim-bookworm

# Checkout and install dagster libraries needed to run the gRPC server
# exposing your repository to dagit and dagster-daemon, and to load the DagsterInstance

RUN apt update && apt install -yqq build-essential git

ADD requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

ENV DAGSTER_HOME=/dagster_home/

RUN mkdir -p $DAGSTER_HOME

WORKDIR $DAGSTER_HOME
