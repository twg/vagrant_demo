# Vagrant Demo

## Before we begin

#### 1. Install VirtualBox

[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

#### 2. Install Vagrant

[http://www.vagrantup.com/downloads](http://www.vagrantup.com/downloads)


#### 3. Download the Ubuntu Trusty64 Base Box

```
$ vagrant box add ubuntu/trusty64
```
 
## Basic VM from scratch


#### Create a default Vagrantfile

```
$ cd 000_basic
$ vagrant init ubuntu/trusty64
```

#### Start the VM

```
vagrant up
```

#### Connect

```
vagrant ssh
```

#### Disconnect

```
exit
```

#### Restart and Stop the VM

```
vagrant reload
vagrant halt
```

#### Destroy the VM

```
vagrant destroy
```

## Synced Folders

#### Start the VM

```
cd 001_synced_folders
vagrant up
```

#### Connect and explore

```
vagrant ssh
ls /vagrant
less /sync_test/hello.txt
```

#### Destroy the VM

```
exit
vagrant destroy
```