# This docker image will be based on ubuntu:19.10
FROM ubuntu:19.10
# Install Python3
RUN apt update && apt install -y python3
# Install Python3 pip package manager for future python related module updates
RUN apt-get install -y python3-pip
# Install Paramiko
RUN pip3 install paramiko
# Install Ansible
RUN apt-get install -y ansible
# Install networking utilities
RUN apt-get install -y traceroute && apt-get install -y net-tools && apt-get install -y iputils-ping
# make a directory for ansible
RUN mkdir -p /home/ansible
# make new directory as working directory when image boots up
WORKDIR /home/ansible
# Also make a packages directory
RUN mkdir -p /home/my-classes
# make port 22 reachable from the host
EXPOSE 22
# install text editors
RUN apt-get install -y vim
# install nano, just in case!
RUN apt-get install -y nano
# required fo ansbile
RUN apt-get install sshpass
