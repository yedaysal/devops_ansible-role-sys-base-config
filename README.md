devops_ansible-role-system-configuration
=========

Ansible role that performs system configuration tasks.

Requirements
------------

This role does not have any requirements.

Role Variables
--------------

This role's variables are located at `devops_main/ansible/group_vars/all/vars.yml` (high priority) and `devops_ansible-role-system-configuration/defaults/main.yml` (low priority):

```yml
# aa_system-configuration role vars
system_max_use: 2G # Controls how much disk space the journal may use up at most.
max_retention_time: 10d # The maximum time to store journal entries.
```

Dependencies
------------

This role does not have any dependencies.

Example Playbook
----------------

This role is included in `devops_main/ansible/plays/base.yml`:

```yml
- name: Ensure base config for all nodes
  hosts: all
  become: true
  roles:
    - base
    - aa_filebeat
    - aa_metricbeat
    - aa_system-configuration
```

License
-------

There is no license for this role.

Author Information
------------------

akakce-devops (devops@akakce.com)
