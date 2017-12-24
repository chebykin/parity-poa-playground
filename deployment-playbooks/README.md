# How to Deploy POA Playground Guide

## Requirements

* Ubuntu 16.04 LTS machine.
* You keys should be added to `root` account of the machine.
* Password authentication should be disabled as the playbook will add a user with a hardcoded password.

## Setting Up POA Playground

* Install Ansible http://docs.ansible.com/ansible/latest/intro_installation.html.
* Clone this repo.
* `cd` into project's `deployment-playbooks` folder.
* Edit `hosts` file and change `192.168.1.101` IP address to the address of your machine.
* Run `deploy.sh` script which is a shortcut for `ansible-playbook -i hosts docker.yml`.
* Wait a few minutes for the installation process finishes.

## Result
After reproducing the steps above you will have the following ports opened on the remote machine:

* 3001 - `ethstats` dashboard
* 8545 - JSON-RPC interface
* 8546 - WebSocket interface
* 8180 - Parity Wallet Web Interface

Also there will be `hacker` user created with `hacker` password.
