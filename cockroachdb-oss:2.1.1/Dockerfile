FROM ubuntu:18.04

RUN apt-get update -y
RUN apt-get install -y wget autoconf libncurses-dev build-essential golang cmake
RUN apt-get clean

RUN wget -qO- https://binaries.cockroachdb.com/cockroach-v2.1.1.src.tgz | tar  xvz

WORKDIR /cockroach-v2.1.1
RUN make buildoss
RUN make install

RUN rm -rf /cockroach-v2.1.1

EXPOSE 8080/tcp
EXPOSE 26257/tcp

CMD cockroach start --insecure
