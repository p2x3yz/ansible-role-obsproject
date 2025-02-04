# [obsproject](#obsproject)

Install obsproject on your system.

|GitHub|GitLab|Quality|Downloads|Version|
|------|------|-------|---------|-------|
|[![github](https://github.com/robertdebock/ansible-role-obsproject/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-obsproject/actions)|[![gitlab](https://gitlab.com/robertdebock/ansible-role-obsproject/badges/master/pipeline.svg)](https://gitlab.com/robertdebock/ansible-role-obsproject)|[![quality](https://img.shields.io/ansible/quality/42908)](https://galaxy.ansible.com/robertdebock/obsproject)|[![downloads](https://img.shields.io/ansible/role/d/42908)](https://galaxy.ansible.com/robertdebock/obsproject)|[![Version](https://img.shields.io/github/release/robertdebock/ansible-role-obsproject.svg)](https://github.com/robertdebock/ansible-role-obsproject/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: robertdebock.obsproject
```

The machine needs to be prepared. In CI this is done using `molecule/default/prepare.yml`:
```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: robertdebock.bootstrap
    - role: robertdebock.epel
    - role: robertdebock.rpmfusion
```

Also see a [full explanation and example](https://robertdebock.nl/how-to-use-these-roles.html) on how to use these roles.


## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/robertdebock/ansible-role-obsproject/blob/master/requirements.txt).

## [Status of used roles](#status-of-requirements)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[robertdebock.bootstrap](https://galaxy.ansible.com/robertdebock/bootstrap)|[![Build Status GitHub](https://github.com/robertdebock/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-bootstrap/actions)|[![Build Status GitLab ](https://gitlab.com/robertdebock/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/robertdebock/ansible-role-bootstrap)|
|[robertdebock.epel](https://galaxy.ansible.com/robertdebock/epel)|[![Build Status GitHub](https://github.com/robertdebock/ansible-role-epel/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-epel/actions)|[![Build Status GitLab ](https://gitlab.com/robertdebock/ansible-role-epel/badges/master/pipeline.svg)](https://gitlab.com/robertdebock/ansible-role-epel)|
|[robertdebock.rpmfusion](https://galaxy.ansible.com/robertdebock/rpmfusion)|[![Build Status GitHub](https://github.com/robertdebock/ansible-role-rpmfusion/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-rpmfusion/actions)|[![Build Status GitLab ](https://gitlab.com/robertdebock/ansible-role-rpmfusion/badges/master/pipeline.svg)](https://gitlab.com/robertdebock/ansible-role-rpmfusion)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/ansible-role-obsproject/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/robertdebock):

|container|tags|
|---------|----|
|debian|all|
|fedora|all|
|ubuntu|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.

## [Exceptions](#exceptions)

Some roles can't run on a specific distribution or version. Here are some exceptions.

| variation                 | reason                 |
|---------------------------|------------------------|
| opensuse | Requires [much more efforts](https://obsproject.com/wiki/install-instructions#opensuse-installation-unofficial) than usual. |
| alpine | obs-studio (missing) |
| centos:latest | nothing provides libSDL2-2.0.so.0()(64bit) needed by ffmpeg-4.2.1-3.el8.x86_64 |
| amazonlinux | Missing dependecies |
| fedora:rawhide | Failure downloading https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-33.noarch.rpm |


If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-obsproject/issues)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[Robert de Bock](https://robertdebock.nl/)

Please consider [sponsoring me](https://github.com/sponsors/robertdebock).
