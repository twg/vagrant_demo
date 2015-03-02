# Vagrant Demo

## Setup

#### 1. Install VirtualBox

[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

#### 2. Install Vagrant

[http://www.vagrantup.com/downloads](http://www.vagrantup.com/downloads)


#### 3. Download the Ubuntu Trusty64 Base Box

```
$ vagrant box add ubuntu/trusty64
```
 
## 0. Basic VM from scratch


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

## 1. Synced Folders

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
exit
```

#### Destroy the VM

```
vagrant destroy
```

## 2. Basic Provisioning

#### Start the VM

```
cd 002_basic_provisioning
vagrant up
```

#### Connect and view example 'provisioning log'

```
vagrant ssh
less ~/provision.log
exit
```

#### Disconnect and do a manual provisioning run

```
vagrant provision
vagrant ssh
less ~/provision.log
exit
```

#### Destroy the VM

```
vagrant destroy
```

## 3. Advanced Provisioning

#### Start the VM

```
cd 003_advanced_provisioning
vagrant up
```

#### Connect and enjoy

```
vagrant ssh
sl
exit
```

#### Destroy the VM

```
vagrant destroy
```

## 4. Multi-Machine

#### Start the VMs (plural!)

```
cd 004_multi-machine
vagrant up
```

#### Connect to each VM

```
vagrant ssh app
exit
vagrant ssh db
exit
```

#### Control VMs individually

```
vagrant halt app
vagrant up app
```

#### Shutdown and destroy VMs

```
vagrant destroy
```

## 5. Networking

#### Start the VM

```
cd 005_networking
vagrant up
```

#### View the nginx default page in your browser

* Via localhost: [http://locahost:8080](http://localhost:8080)
* Via the private network: [http://10.0.0.101](http://10.0.0.101)

##### _Aside: [Vagrant DNS](https://github.com/BerlinVagrant/vagrant-dns)_

##### _Aside: [Pow](http://pow.cx)_

Localhost:

* `echo 8080 > ~/.pow/myapp`

Private network:

* `echo http://10.0.0.101 > ~/.pow/myapp`


#### Shutdown and destroy VMs

```
vagrant destroy
```

## Further Reading

#### Plugins

[http://docs.vagrantup.com/v2/plugins/index.html](http://docs.vagrantup.com/v2/plugins/index.html)

#### Providers

[http://docs.vagrantup.com/v2/providers/index.html](http://docs.vagrantup.com/v2/providers/index.html)

#### Ansible

[http://www.ansible.com/resources](http://www.ansible.com/resources)

#### Docker

[https://www.docker.com](https://www.docker.com)