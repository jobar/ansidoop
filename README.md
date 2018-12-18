# Ansible Hadoop / Hive / Spark installation using BigTop on Ubuntu

## Requirement

* ansible must be installed on the host launching the installation.
* An SSH-key with an accessible private-key pem file should allow to connect
without password to every host defined in the `hosts` file. The signatures
of the various hosts should also be added to the running host know-hosts.
You can test the ssh-keys and known-hosts setup after having updated the
`hosts` file using:
```
ansible -i hosts all --key-file /PATH/TO/THE/PEM/FILE -m ping
```

## Configuration

Update the `hosts` and `group_vars/all` files to your needs (don't forget
the private ssh-key file at the beginning of the variables file).

## Installation
```
ansible-playbook -i hosts setup_cluster.yml
```

## Acknowledgement

This repo has been widely copied and modified from
[ElastiCluster](http://gc3-uzh-ch.github.io/elasticluster/).

----
Copyright (C) 2018  JoalTech - https://www.joaltech.com
