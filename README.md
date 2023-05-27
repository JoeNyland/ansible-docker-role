joenyland.docker
================

[![CI](https://github.com/JoeNyland/ansible-docker-role/actions/workflows/ci.yml/badge.svg)](https://github.com/JoeNyland/ansible-docker-role/actions/workflows/ci.yml)

Installs [Docker (CE)](https://www.docker.com/).

Requirements
------------

None.

Role Variables
--------------

### `docker_users`

A list of users who should be able to use Docker on the target hosts.

This adds the requested users to the `docker` group on the target hosts, which allows them to communicate with the Docker daemon without root access.

More info https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user

### `docker_daemon_config`

A hash of configuration to be stored in `/etc/docker/daemon.json`.

Allows configuration of the Docker daemon.

E.g.

```yaml
docker_daemon_config:
  experimental: true
  ipv6: true
  ip6tables: true
  fixed-cidr-v6: 2001:aaaa:bbbb:ccc::/64
  registry-mirrors:
    - https://registry.ipv6.docker.com
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: server
  roles:
    - joenyland.docker
```

License
-------

MIT

Author Information
------------------

⌨️ with ❤️ by [Joe Nyland](https://joe.nyland.io)
