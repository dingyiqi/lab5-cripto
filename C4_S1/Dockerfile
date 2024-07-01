# Dockerfile.22.10
FROM ubuntu:22.10

RUN sed -i 's|http://archive.ubuntu.com/ubuntu/|http://old-releases.ubuntu.com/ubuntu/|g' /etc/apt/sources.list && \
	sed -i 's|http://security.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|g' /etc/apt/sources.list && \
	apt-get update && \
	apt-get install -y openssh-client openssh-server && \
	useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 test \
    && echo 'test:test' | chpasswd
	
EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]






