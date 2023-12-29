FROM ubuntu:22.04

ENV TZ Asia/Seoul
ENV PYTHONIOENCODING UTF-8
ENV LC_CTYPE C.UTF-8

RUN apt-get update && apt-get upgrade
RUN apt-get install -y socat gdb git gcc curl wget vim ruby ruby-dev
RUN apt-get install -y python3 python3-pip python3-dev libssl-dev libffi-dev build-essential
RUN apt-get install -y net-tools openssh-server

RUN python3 -m pip install --upgrade pip

RUN pip3 install pwntools ropgadget
RUN gem install one_gadget
RUN gem install seccomp-tools

RUN git clone https://github.com/pwndbg/pwndbg.git
RUN cd pwndbg && ./setup.sh

RUN echo 'source /pwndbg/gdbinit.py' >> /root/.gdbinit

WORKDIR /root

EXPOSE 22
