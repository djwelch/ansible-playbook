# My ansible playbook

## Goal

Be able to spin up a new development environment with my normal configuration quickly and easily.

## Setup

Uses ansible.  To configure the PPA on your machine and install ansible run these commands:

```
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

## Keep secrets

```
ansible-vault encrypt <filename> --vault-password-file ~/.ansible_vault_password
```

## Run the playbook

```
ansible-playbook setup.yml -i HOSTS -K --vault-password-file ~/.ansible_vault_password
```

## After running

Need to sort this stuff out:
 - have to install the vim plugins.
 - vim-parinfer needs compilation.
 - the java ca certs thing still fails unless you run the playbook twice?

## License

MIT © David Welch
