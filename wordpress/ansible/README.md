# Deploy Wordpress on OpenStack using Ansible

## Authenticate to OpenStack

```
source <cloudrc.sh file>
```

## Install openstack.cloud

```
ansible-galaxy collection install -r requirements.yml
```

## Define variables

Change variables in variables.yml file to match your environment configuration.

Variables are:
- image: Image to use for instances
- flavor: Flavor to use for instances
- key_name: Name of the keypair to link to instances
- db_name: WordPress database name
- db_username: The WordPress database admin account username
- db_password: The WordPress database admin account password
- db_root_password: Root password for MySQL
- floating_network_id: name of public network


## Create environment

```
ansible-playbook playbook.yml
```


## Destroy environment

```
ansible-playbook destroy.yml
```

