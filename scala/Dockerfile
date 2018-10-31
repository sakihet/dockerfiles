FROM openjdk:10

# install sbt
RUN \
  echo "deb https://dl.bintray.com/sbt/debian /" > /etc/apt/sources.list.d/sbt.list && \
  apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823 && \
  apt-get update && \
  apt-get install sbt

RUN mkdir /app
WORKDIR /app

COPY build.sbt /app/build.sbt
RUN sbt update
