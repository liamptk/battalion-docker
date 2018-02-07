# Dockerfile for the Battalion 1944 Community Server 
FROM ubuntu:latest
MAINTAINER Liam Kelly <liamptk@gmail.com>

# Environment Variables

ENV BATTALIONDIR="/battalion"
ENV BATTALIONDL="https://storage.googleapis.com/battalion_public/BattalionLinuxServer_10849.zip"
ENV BATTALIONZIP="BattalionLinuxServer_10849.zip"
ENV BATTALIONRUN="$BATTALIONDIR/LinuxServer/Run.sh"


# Download, unzip and run the server

RUN apt-get -y update && \
    apt-get -y install unzip && \
    apt-get -y install wget && \
    wget "$BATTALIONDL" && \
	mkdir -p "$BATTALIONDIR" && \
    unzip "$BATTALIONZIP" -d "$BATTALIONDIR" && \
    "./$BATTALIONRUN"
    

ENTRYPOINT ["$BATTALIONDIR"]