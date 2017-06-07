# HTTPS Servers Cheat Sheet

Repository containing vagrant configurations for how to properly install and
harden common web servers,  as well as configuration for meeting requirements
for (e.g.) HTTPS and HSTS, as laid out in [OMB
M-15-13](https://obamawhitehouse.archives.gov/sites/default/files/omb/memoranda/2015/m-15-13.pdf) /
[The HTTPS-Only Standard](https://https.cio.gov)

## Setup

This project makes heavy use of [Vagrant](https://www.vagrantup.com) and
[VirtualBox](https://www.virtualbox.org) for managing the reference
environments. For more information about installing those tools, see their
respective documentation.

### Local host names

This project uses the hostname ``vagrant.local`` for the default IP address
defined in the Vagrant files, to make use of this hostname, you will need to add
it to your local ``/etc/hosts`` file on the VM host, and restart your networking. 

#### macOS

```bash
echo "192.168.33.10   vagrant.local" >> /etc/hosts
sudo killall -HUP mDNSResponder
```

#### Linux

```bash
echo "192.168.33.10   vagrant.local" >> /etc/hosts
```

Changes should take effect immediately.

### Quickstart

```bash
cd el7/
vagrant up
open https://vagrant.local

# Optional if you have pshtt installed (https://github.com/dhs-ncats/pshtt)
pshtt vagrant.local
```

## Release

HSCS is released under an [MIT License](LICENSE.md).

Produced at Lawrence Livermore National Laboratory, LLNL-CODE-732135
