# cicd-web-project
Jenkins-CI-CD-Pipeline

# Docker Server settings

> # vi /etc/sysconfig/docker

```
# /etc/sysconfig/docker

# Modify these options if you want to change the way the docker daemon Exercises
OPTIONS="--selinux-enabled=false --log-driver=journald --signature-verification=false'

if [ -z "${DOCKER_CERT_PATH}" ]; then
    DOCKER_CERT_PATH=/etc/docker
fi
```

> # yum install -y iptables net-tools

> # sed -i -e 's/overlay2/vfs/g' /etc/sysconfig/docker-storage

> # systemctl start docker
