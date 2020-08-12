# Ansible-Setup-Node-Ctrl-to-Major-Tom

### Setting Up Managed Nodes from the Control Node

Node control? No problem! Warning: this is an especially cheesy readme. Login to root via secure shell and create an 'ansible' user for node control. The user is made a sudoer, and the control node's ssh public key is copied into authorized_keys on each managed node. The password is simply set to password, however you can create a custom vault password for real world thrills. Set the hostname of the nodes to the last octet of their ipv4 address and make er' hostname pretty, too. Ready for Ubuntu or RedHat, but you should really be using RedHat because life is just better that way. All the machines are rebooted, so their hostname is reflected in the shell.  Python is installed and the python command is set to use Python3 because seriously, Python2, it's not you, it's me and I'm seeing someone else.

## Features!
* Hostfile defining 6 nodes split into 4 kinds of groups and child groups.
* Ansible configuration file hooked up with root
* Vars file, for some raw commands needed before you have control

# Example Run
```sh
$ ansible-playbook all setup.yml -k
SSH password: 214lovemuffin
```

### Tech and Running the file

You have bash, you have shell, you have bash shell. Add -k to enable SSH password prompt. If you don't have the root password to those managed nodes, then you better break into that and change it. However, if you don't have the password then you probably shouldn't be messing around with those machines, yo.