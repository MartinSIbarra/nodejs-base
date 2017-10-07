# Development local

* Para iniciar la maquina local desde cero

```
# Instalar cygwin + apt-cyg
# Instalar VirtualBox
# Instalar Vagrant
# Instalar Ansible
apt-cyg install make automake gcc-g++ python3-devel
apt-cyg install python3-pip
CFLAGS="-g -O2 -D_BSD_SOURCE" python3 -m pip install -U pycrypto
python3 -m pip install -U ansible

# Clonar este repositorio
vagrant plugin install vagrant-vbguest
git submodule init && git submodule update
vagrant up
```
