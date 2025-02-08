ansible_userspace
=================
[![Ansible Lint](https://github.com/oxivanisher/role-ansible_userspace/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-ansible_userspace/actions/workflows/ansible-lint.yml)

This role confgures a Python virtual environment for Ansible in a users home.

Notes
-----

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

| Name                          | Comment                                                                              | Default value      |
|-------------------------------|--------------------------------------------------------------------------------------|--------------------|
| ansible_userspace_user        | Which user will be configured                                                        | `root`             |
| ansible_userspace_venv_subdir | Which subdirectory in the users home will be used for the python virtual environment | `dev/ansible-venv` |

Example Playbook
----------------

```yaml
- name: Userspace Ansible Environment
  hosts: jumphosts
  roles:
    - role: oxivanisher.linux_server.ansible_userspace
      tags:
        - ansible
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_server](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_server/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_server).
