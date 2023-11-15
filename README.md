# Ubuntu laptop Ansible Playbook

The playbook installs and configures most of the software I use on my machine which runs Ubuntu.

## Installation

1. [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html):

    1. Update apt: `sudo apt update`
    2. Install Ansible: `sudo apt install ansible`
    3. Check ansible version: `ansible --version`

2. Clone or download this repository to your local drive.
3. Run `ansible-galaxy install -r requirements.yml` inside this directory to install required Ansible collections.
4. Run `ansible-playbook main.yml --ask-become-pass` inside this directory.

## Testing the playbook

Testing is done via using Vagrant where `Vagrantfile` and a `test_vagrant.yml` files are used to test the configuration.

- Install Vagrant by following the [documentation](https://developer.hashicorp.com/vagrant/docs/installation)

- Create a Vagrant box and provision it

  ```bash
  vagrant up --provision
  ```

- Force destroy and recreate the box

  ```bash
  vagrant destroy --force && vagrant up --provision
  ```

> Vagrantfile will use `test_vagrant.yml` file as the `Ansible` entrypoint.
>
> Box name `generic/ubuntu2304` - <https://app.vagrantup.com/generic/boxes/ubuntu2304>
>
> Box link - <https://app.vagrantup.com/boxes/search>

Here is link to install Vagrant with using [libvirt](https://vagrant-libvirt.github.io/vagrant-libvirt/)
