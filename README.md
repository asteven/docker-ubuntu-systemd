# docker-ubuntu-systemd

A Ubuntu based docker image that runs systemd as pid 1.


## Usage

```
sudo podman run -d \
   --name ubuntu --hostname ubuntu \
   --tmpfs /tmp --tmpfs /run --tmpfs /run/lock \
   -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
   docker.io/asteven/ubuntu-systemd
```

```
sudo podman exec -ti ubuntu /bin/bash
```

```
sudo podman rm --force ubuntu
```
