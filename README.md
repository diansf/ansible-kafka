# Ansible Playbook for Kafka Cluster

## Overview
An ansible role to install and configure kafka clusters.

### Supported Platforms
- Debian
- Ubuntu

### Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites
Prerequisite Package :
```
ansible==2.6.20
cryptography==2.5
```

Just run ```pip install -r requirements.txt``` for install prerequisite packages

### How to Run
Before run ansible playbook please prepare for vault variable that store in group_vars.

- Create Vault Variable
```
ansible-vault encrypt_string 'zookeeper#Passw0rd-groupvars-vault' --name 'zookeeper_admin_password' --vault-password-file ~/.ansible/vault-pass
```

```
ansible-vault encrypt_string 'kafka#Passw0rd-groupvars-vault' --name 'kafka_admin_password' --vault-password-file ~/.ansible/vault-pass
```

- Run Playbook
```
ansible-playbook --vault-password-file ~/.ansible/vault-pass deploy-kafka.yml
```

## Authors

* **Aas Suhendar** - *Initial Work* - [AasSuhendar](https://github.com/AasSuhendar)
* **Dimas Restu Hidayanto** - *Initial Work* - [DimasKiddo](https://github.com/dimaskiddo)

See also the list of [contributors](https://github.com/AasSuhendar/ansible-kafka/contributors) who participated in this project
