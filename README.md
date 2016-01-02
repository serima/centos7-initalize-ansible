# centos7-initalize-ansible

## Requirements

### Host

* Ansible 1.9

### Client

* CentOS 7
  - The state that installation of CentOS 7 is completed
  - Set up a root password

## Usage

First, you need to edit hosts file.

```
% user_password=$(openssl passwd -salt salty -1 <PASSWORD>)
% ansible-playbook -k -c paramiko -i hosts sakura_init.yml -vvv --extra-vars "user_password=$user_password"
```
