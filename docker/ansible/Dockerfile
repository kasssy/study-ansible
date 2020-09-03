FROM centos:7

ENV ANSIBLE_HOST_KEY_CHECKING False

# openssh-clientsはansible実行する上で必須
# vimはお試しついでにinstall
RUN yum install -y epel-release && \
    yum install -y openssh-clients && \
    yum install -y vim && \
    yum install -y ansible

