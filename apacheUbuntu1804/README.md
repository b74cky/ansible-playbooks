Role Name
=========

Apache2 Ubuntu 18.04

This role will Install the Apache 2 web server on an Ubuntu 18.04 machine and create a virtualhost with the options specified in 'vars/apacheVars.yml' file.

Requirements
------------

- An Ubuntu 18.04 machine should be created
- Have a remote non-root user on the instance to own the Apache files (should be specified in `app_user` variable) 

Role Variables
--------------

All vars are specified in 'vars/apacheVars.yml':

- `app_user`: a remote non-root user on the host that will own the app files
- `http_host`: domain name
- `http_conf`: the name of Apache conf file
- `http_port`: HTTP port, 80 by default 
- `disable_default`: whether or not to disable the default Apache website. When set to true, your virtualhost will be used as default website

Example Playbook
----------------

1) Clone the playbook and dig into it

```shell
git clone https://github.com/yauhenidasko/ansible-playbooks
cd ansible-playbook/apacheUbuntu1804
```

2) Customize the values of variables

```shell
vi vars/apacheVars.yml 
```

3) Run the Playbook

```command
ansible-playbook -l [target] -i [inventory file] -u [remote user] main.yml
```

License
-------

MIT

