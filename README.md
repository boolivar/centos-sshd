# centos-sshd
Systemd enabled container with openssh-server
### Run with the cgroups filesystem mounted
`docker run -d -P -v /sys/fs/cgroup:/sys/fs/cgroup:ro boolivar/centos-sshd:latest`
### Run on Ubuntu host
`docker run -d -P -v /sys/fs/cgroup:/sys/fs/cgroup:ro -v /tmp/$(mktemp -d):/run boolivar/centos-sshd:latest`
### Run in privileged mode
`docker run -d -P --privileged boolivar/centos-sshd:latest`