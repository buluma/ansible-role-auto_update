# Ansible role [auto_update](https://galaxy.ansible.com/ui/standalone/roles/buluma/auto_update/documentation)

Install and configure automatic package updates on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-auto_update/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-auto_update/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-auto_update.svg)](https://github.com/buluma/ansible-role-auto_update/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-auto_update.svg)](https://github.com/buluma/ansible-role-auto_update/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-auto_update.svg)](https://github.com/buluma/ansible-role-auto_update/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/auto_update)](https://galaxy.ansible.com/ui/standalone/roles/buluma/auto_update/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-auto_update/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: buluma.auto_update
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-auto_update/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-auto_update/blob/master/defaults/main.yml):

```yaml
---
# defaults file for auto_update

# (RedHat like systems only) What type of updates to apply, valid choices are:
# default, security, security-severity:Critial, minimal, minimal-security, minimal-security-severity:Critical
auto_update_update_cmd: default

# (RedHat like systems only) Whether a message should be emitted when updates are available, were downloaded, or applied.
auto_update_message: no

# Whether updates should be downloaded when they are available.
auto_update_download_updates: yes

# Whether updates should be applied when they are available.  Note
# that download_updates must also be yes for the update to be applied.
auto_update_apply_updates: no

# Maximum amout of time to randomly sleep, in minutes.
auto_update_random_sleep: 360
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-auto_update/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.cron](https://galaxy.ansible.com/buluma/cron)|[![Ansible Molecule](https://github.com/buluma/ansible-role-cron/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-cron/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-cron.svg)](https://github.com/shadowwalker/ansible-role-cron)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-auto_update/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/repository/docker/buluma/enterpriselinux/general)|8|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|all|
|[Fedora](https://hub.docker.com/repository/docker/buluma/fedora/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-auto_update/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-auto_update/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-auto_update/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)

