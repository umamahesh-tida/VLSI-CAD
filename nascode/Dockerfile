FROM nvidia/cuda:12.3.2-cudnn9-runtime-ubuntu20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get install -y git
RUN apt-get install python3-pip
RUN apt get install python3-dev
RUN apt-get install python3-opencv
RUN apt-get install libglib2.0.0

RUN python3 -m pip install --upgrade pip

RUN pip3 install torch torchvision torchaudio -f https://download.pytorch.org/whl/cu111/torch_stable.html

COPY . /app
WORKDIR /app