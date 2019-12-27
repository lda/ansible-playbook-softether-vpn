# About

Ansible playbook example which helps you install and configure Softether VPN on your own server instance (only CentOs is currently supported)

# Prepare your workstation

## Install Ansible

### OS X
```
brew install ansible
```

### Ubuntu
```
apt-get install ansible
```

### CentOS
```
yum install ansible
```

## Clone project with submodules
```
git clone --recursive https://github.com/lda/ansible-playbook-softether-vpn.git
cd ansible-playbook-softether-vpn
```

## Configure project

### Configure vpn
```
cp ansible/vars/vpn.yml.example ansible/var/vpn.yml
```

Open `ansible/var/vpn.yml` in your favorite editor and change the values.

### Configure hosts file
```
cp ansible/inventory.example ansible/inventory
```

Open `ansible/inventory` in your favorite editor and change the values.

## Install Softether VPN Server
```
ansible-playbook -i ansible/inventory ansible/playbook.yml
```