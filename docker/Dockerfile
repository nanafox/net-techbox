# this docker file is used for network testing and monitoring
# it contains enough tools to thoroughly test a network.
# The technician use a few pen test tools to further confirm the security of the network


# use the latest Ubuntu image
FROM ubuntu

# maintainer's details
LABEL author.name="Maxwell Nana Forson"
LABEL author.email="nanaforsonjnr@gmail.com"
LABEL author.github="https://github.com/nanafox"
LABEL version="1.0"

# set working directory to the home of root user
WORKDIR /root

# update and install required tools
RUN apt update
RUN apt install -y isc-dhcp-client tftp openssh-server vsftpd
RUN apt install -y rsyslog rsyslog-snmp snmp snmpd snmptrapd

# network connectivity testing tools
RUN apt install -y net-tools iproute2 bash-completion \
    inetutils-traceroute iputils-ping iputils-tracepath \
    iputils-arping

# install CLI network capture tools - Tshark can be manually installed
RUN apt install -y nmap tcpdump dsniff htop

# firewall and security tools
RUN apt install -y ufw nftables 

# IP Address tools and text editors
RUN apt install -y ipcalc-ng vim nano less

# add needed files
ADD README.md /net-techbox.README.md
ADD docker/banner.txt /etc/motd
ADD scripts /scripts

# Add a few aliases
ADD docker/bash_aliases /root/.bash_aliases
RUN echo "cat /etc/motd" >> /etc/bash.bashrc
ENV PATH $PATH:/scripts
