VirtualBox Specific
===================

The following have been added to the image (in addition to those listed in [README.md](README.md)):

  * bzip2, dkms, gcc, perl, and VBoxGuestAdditions are installed
  * Root password is set to *root*

To build a VirtualBox box:

  1. `rm -f /tmp/packer-centos-7.3.1611-x86_64-updates-vbox-*`
  1. `packer build --only=vbox4vbox centos-7.3.1611-x86_64-updates.json`
  1. Launch `/tmp/packer-centos-7.3.1611-x86_64-updates-vbox-*/*.vmdk` in VirtualBox
  1. Smoke test (e.g., login via console and look around)
