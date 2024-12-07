FROM ubuntu:22.10
RUN sed -i 's|http://archive.ubuntu.com/ubuntu/|http://old-releases.ubuntu.com/ubuntu/|g' /etc/apt/sources.list && \
    sed -i 's|http://security.ubuntu.com/ubuntu|http://old-releases.ubuntu.com/ubuntu|g' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install openssh-client -y openssh-server && \
    useradd -m -s /bin/bash prueba && \
    echo 'prueba:prueba' | chpasswd && \
    mkdir -p /var/run/sshd
EXPOSE 22
#para que el servidor permanezca activo
CMD ["/usr/sbin/sshd", "-D"]




