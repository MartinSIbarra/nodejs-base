# Development local

## Para iniciar la maquina local desde cero
* Instalar VirtualBox
* Instalar Vagrant
* Instalar Babun
```
# Configuracion extra para que vagrant fucione bien en babun
echo export VAGRANT_DETECTED_OS=dummy >> ~/.zshrc
```

* Instalar Ansible
```
# Dentro de una terminal babun
cd # para ejecutarlo en el home
curl -s https://raw.githubusercontent.com/tiangolo/ansible-babun-bootstrap/master/install.sh | source /dev/stdin

```

* Instalar roles ansible
```
ansible-galaxy install geerlingguy.nodejs
```

* Clonar este repositorio

* Instalar plugin vagrant virtualbox guest additions
```
vagrant plugin install vagrant-vbguest
```

* Levantar maquina 
```vagrant up```

* Provisionar maquina
```
ansible-playbook --private-key=.vagrant/machines/default/virtualbox/private_key -u vagrant -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory playbook.yml
```
