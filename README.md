# Ansible_playbook_demo

## Playbooks
This repo contains the following ansible playbooks

- playbook.yml : for testing, and you can ignore.
- ssh_playbook.yml: This is the one you should use.

## What playbook does
The `ssh_playbook.yml` contains ansible tasks to provision users on a virtual machine (ubuntu, in this case) each with their own public SSH key added to their `authorized_key` files.

## Adding more users to virtual machine
You can add as many users and their corresponding public key as you want in the `users.yml` file

## Commands
This repo does not include a github `workflow` file, so you should have ansible installed on your local machine/laptop and run the commands below

1. Modify the `inventory.hosts` file with the correct `ansible_user` and `ansible_ssh_private_key_file`

2. Replace public keys and user names in `users.yml`

3. Add the public IP address of the remote hosts you want to configure in the `inventory.hosts` file

4. Run the command below
```
ansible-playbook ssh_playbook.yml
```

## Further Reading
See [here](https://medium.com/@chandrapal/managing-linux-users-ssh-keys-using-ansible-39ee2fc24c16)