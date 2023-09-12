FROM centos:centos7

ENV container docker
USER root

RUN yum update -y

RUN rpm --import https://repo.saltproject.io/salt/py3/redhat/7/x86_64/SALT-PROJECT-GPG-PUBKEY-2023.pub
RUN curl -fsSL https://repo.saltproject.io/salt/py3/redhat/7/x86_64/latest.repo | tee /etc/yum.repos.d/salt.repo
RUN yum clean expire-cache
RUN yum install -y \
 salt-minion

CMD ["salt-minion"]