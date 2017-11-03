FROM golang:latest
MAINTAINER vmarmol@google.com

RUN apt-get update && apt-get install -y git dmsetup && apt-get clean
RUN git clone https://github.com/wroujoulah/cadvisor.git /go/src/github.com/wroujoulah/cadvisor
RUN cd /go/src/github.com/wroujoulah/cadvisor && make

ENTRYPOINT ["/go/src/github.com/google/cadvisor/cadvisor"]

