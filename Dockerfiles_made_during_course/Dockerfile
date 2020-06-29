FROM ubuntu
LABEL AUTHOR="Martins Tararujs" COMPANY="TestDevLab"

ARG APIMATION_VERSION=0.54.7
ENV VERSION=${APIMATION_VERSION}

RUN apt update
RUN apt upgrade
RUN apt install -y curl

WORKDIR /usr/src/apimation
RUN apt install wget
RUN apt install -y unzip
RUN wget https://github.com/apimation/cli-client/releases/download/v${APIMATION_VERSION}/apimation_${APIMATION_VERSION}_linux_amd64.zip
RUN unzip apimation_${APIMATION_VERSION}_linux_amd64.zip
RUN rm apimation_${APIMATION_VERSION}_linux_amd64.zip

ENTRYPOINT ["./apimation" ]