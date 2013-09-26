# Packer Templates

This is a set of templates designed for use with Packer to make VMware and VirtualBox images.

Templates:
- CentOS 6.4

# Usage

- Install [Packer](http://www.packer.io/)
- Clone this [repository](https://github.com/webcoyote/packer-templates.git
- Edit the security credentials
- Run the "./build" (Linux/OSX) or "build.bat" (Windows)

# Security

If you're planning on building a secure system you'll want to set your own passwords and SSH keys. Edit these files:

- [centos-6.4-x86_64-netboot/http/ks.cfg](https://github.com/webcoyote/packer-templates/blob/master/centos-6.4-x86_64-netboot/http/ks.cfg): rootpw and vagrant password
- [centos-6.4-x86_64-netboot/template.json](https://github.com/webcoyote/packer-templates/blob/master/centos-6.4-x86_64-netboot/template.json): vagrant password
- [centos-6.4-x86_64-netboot/scripts/vagrant.sh](https://github.com/webcoyote/packer-templates/blob/master/centos-6.4-x86_64-netboot/scripts/vagrant.sh): vagrant public SSH key

### rootpw

Use the Ruby [UnixCrypt](https://github.com/webcoyote/unix-crypt) gem to create an encrypted password or you can remove the "--iscrypted" flag to use an unencrypted password string.

### vagrant

Redefine the vagrant account name ("vagrant"), password ("vagrant") and [SSH key](https://raw.github.com/mitchellh/vagrant/master/keys/vagrant.pub). You will also need to update your Vagrantfile to use these changed credentials.

# Credits

This template is based on https://github.com/smerrill/packer-templates

- Author: Steven Merrill (steven.merrill@gmail.com)
- Contributions: Patrick Wyatt (pat@codeofhonor.com)

