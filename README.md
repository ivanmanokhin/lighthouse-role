lighthouse-role
=========

Role for installation LightHouse on RHEL

Requirements
------------

- nginx
- git

Role Variables
--------------

| var | description |
| - | - |
| `lighthouse_branch` | Branch on [lighthouse](https://github.com/VKCOM/lighthouse) repo |

Dependencies
------------

[ansible-clickhouse](https://github.com/AlexeySetevoi/ansible-clickhouse.git)

Example Playbook
----------------

Example of using a role:

  ```yaml
  - hosts: servers
    pre_tasks:
      - name: Install EPEL-release
        become: true
        ansible.builtin.yum:
          name: epel-release
      - name: Install Git
        become: true
        ansible.builtin.yum:
          name: git
      - name: Install Nginx
        become: true
        ansible.builtin.yum:
          name: nginx
    roles:
       - { role: lighthouse-role }
  ```

License
-------

MIT

Author Information
------------------

Ivan Manokhin
