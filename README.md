puppet-kvm
==========

A module for RedHat/CentOS based distros that ensures the KVM required packages are installed
on a node and that the libvirtd service is running as to have a basic management tool for VMs.

This module also configures the bridge interface - as this is the recommended networking mode for QEMU -
and adds by default eth0 in the bridge. This is assuming "eth0" is your main interface. If not, change
the $main_interface parameter to suit your needs.

!! Warning !!
After applying this class you might need to restart networking on the node for the changes to be applied.
This will kill all your current connections so make sure it is not a production machine and you have another
way of logging in the machine in case things go wrong.
