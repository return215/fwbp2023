---
title: "Getting CodeIgniter to work with Podman"
date: 2023-11-06T09:18:29+07:00
draft: false
---

Source code of the project will be shared as soon as possible.

I have to set the correct permissions for Postgres and CI to work. For Postgres, this can be seen from the output of the command `grep postgres /etc/passwd` directly on the image. I can't do it on the running containers itsef becaused it exited before I got the chance to run it, and it says 999. As for CI, it was specified right in the compose file below, which is 9999. So, on the project folder, I run:

```sh
podman unshare chown 999:999 ./db
podman unshare chown 9999:9999 ./app
podman unshare chown 9999:9999 ./ssl
```

Additional work is needed for active SELinux systems. To figure that out, I run the following:

```sh
getenforce
```

Mine says `Enforcing`. But if it shows something else, you don't need to do the following workaround. Docker provides an option to do this, which is to mount the volumes to the containers using the `Z` flag which means "private unshared bind mount". This flag may not be necessary if you are not runnning an enforcing SELinux system. 

My `docker-compose.yml` therefore looks like this:

```yaml
version: '3'
services:
  app-ci4:
    image: shinsenter/codeigniter4:latest
    volumes:
      - ./app:/var/www/html:Z
      - ./ssl:/etc/ssl/web:Z
    environment:
      TZ: UTC
      PUID: ${UID:-9999}
      PGID: ${GID:-9999}
    ports:
      - "8080:80"
      - "8443:443"
    links:
      - "db-pg"
  db-pg:
    image: postgres:12-bullseye
    volumes:
      - ./db:/var/lib/postgresql/data:Z
    environment:
      POSTGRES_PASSWORD: unsecurepassword
```

Relevant articles:

- [Using Podman user namespaces for rootless containers](https://www.redhat.com/sysadmin/user-namespaces-selinux-rootless-containers)
- [Configure SELinux label for bind mounts](https://docs.docker.com/storage/bind-mounts/#configure-the-selinux-label)
