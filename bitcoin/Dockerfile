FROM python:3.6

# Set up code directory
# RUN mkdir -p /usr/src/app
WORKDIR /src

# Install Linux dependencies
RUN apt-get update && apt-get install -y libssl-dev wget \
  && apt install -y netcat-openbsd \
  && wget https://github.com/vagabondan/docker-python/blob/master/bitcoin/requirements.txt
  && pip install -r requirements.txt \
  && pip install -e . \

WORKDIR /app
