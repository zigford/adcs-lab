# adcs-lab

# Caveats

These Vagrantfile and ansible playbooks are written to run on libvirt kvm
hypervisor. Networking and IP addressing are all hard coded for quick
development.

However, it shouldn't be much work to adjust these and make it work on say,
Windows with VirtualBox.

# Requirements

* Libvirt
* Vagrant
* Ansible
* A Samba share on the host for the user `vagrant`
* On the Samba share should be a directory `LabSources` with SQL and SCCM
  sources as subdirectories. 
* The ansible playbooks will look for those installers there.

# Usage

Spinup the systems with `vagrant up`
Install everything in order with `ansible-playbook main.yml` OR
Install the bits individually using their own separate playbooks.
