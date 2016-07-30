# centos7-initalize-ansible

## Requirements

### Host

* Ansible 1.9

### Client

* CentOS 7
  - The state that installation of CentOS 7 is completed
  - Set up a root password

Sakura VPS setup guide is [here](https://help.sakura.ad.jp/app/answers/detail/a_id/2397/~/%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%A0os%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%82%AC%E3%82%A4%E3%83%89---centos7-%2F-scientificlinux7-%2F-fedora-24) (Japanese)

## Usage

First, you need to edit hosts file.

```
% user_password=$(openssl passwd -salt salty -1 <PASSWORD>)
% ansible-playbook -k -c paramiko -i hosts sakura_init.yml -vvv --extra-vars "user_password=$user_password"
```
