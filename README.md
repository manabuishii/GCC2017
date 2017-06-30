# GCC2017

# Require

Microsoft Azure account.

# Deploy



## Simple deployment

This button construct Linux machines that have
docker , job scheduler , automatic machine up and down system.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmanabuishii%2Fazure-files%2Fmaster%2FNFS_SGE%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

## Galaxy deployment

Galaxy cluster and above.

### Master_script

```
https://raw.githubusercontent.com/manabuishii/azure-files/master/scripts_for_setup/galaxy_SGE/master_script.sh
```


### Worker_script

```
https://raw.githubusercontent.com/manabuishii/azure-files/master/scripts_for_setup/galaxy_SGE/exec_script.sh
```

## How to start Galaxy

login and just type

```
/etc/init.d/docker-galaxy start
```

TODO automatically start `/etc/init.d/docker-galaxy`



# Flow

Deployment flow is following

1. Press button and fill the some value (after this step , everything is done automatically)
1. Deployment of machine is started
1. Each machines are deployed , automatically start shell script.
5. Shell script start chef
6. chef setup Linux environment.

# About shellscript to start chef

[See](https://github.com/manabuishii/azure-files)

# TODO

* documentation more
* Support AWS, GCP and other public cloud service
* for openstack, cloudstack
