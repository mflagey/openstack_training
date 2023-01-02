# Deploy Wordpress on OpenStack using Heat

## Authenticate to OpenStack

```
source <cloudrc.sh file>
openstack token issue
```

## Create the stack

in heat folder

```
openstack stack create -t heat.yaml wordpress \ 
    --parameter "image=<debian image name>" \
    --parameter "flavor=<flavor to use>" \
    --parameter "key_name=<your openstack keypair name>" \
    --parameter "floating_network_id=<name of public ip pool>"
```

You can also override database parameters: db_name, db_username, db_password and db_root_password


## Delete the stack

```
openstack stack delete wordpress
```

