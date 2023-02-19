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

Dependencies
------------

None.

Example Playbook
----------------

```yaml
# requirements.yml
roles:
  - name: joenyland.docker
    src: https://github.com/JoeNyland/ansible-docker-role
```

```yaml
# Playbook
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
