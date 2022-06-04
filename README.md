Vector
=========

Разворачивает Vector.

Requirements
------------

ОС: centos7, ubuntu


Role Variables
--------------

`vector_version`: версия
`vector_config`: конфигурация

Example Playbook
----------------

```ansible
- name: Install Vector
  hosts: vector
  roles: 
    - vector
  post_tasks:
    - name: Vector | Add log directory
      ansible.builtin.file:
        path: /home/ansible/logs
        state: directory
        mode: '0755'
```

License
-------

MIT

Author Information
------------------

Arkhipov Evgeniy