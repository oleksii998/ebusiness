FROM ubuntu:18.04

RUN apt update && apt install -y wget \
    openjdk-8-jdk \
    npm

RUN wget http://scala-lang.org/files/archive/scala-2.12.13.deb && dpkg -i scala-2.12.13.deb && apt install scala

RUN wget https://dl.bintray.com/sbt/debian/sbt-1.4.9.deb && dpkg -i sbt-1.4.9.deb && apt install sbt

RUN useradd -ms /bin/bash user1
USER user1
WORKDIR /home/user1

VOLUME ["/home/user1/workspace"]

EXPOSE 9000
EXPOSE 3000