# RHEL 6 + Apache 2.2 Configuration

This vagrant configuration provides a buildable, workable example of installing and configuring Apache 2.2 on RHEL / CentOS 6.

The end state, is one that should pass Tenable and DHS scanners for SSL security, with the exception of using a self signed SSL certificate, since this is a development environment after all.

## Getting Started

To spin up the environment, follow standard ``vagrant up`` process, as defined on https://www.vagrantup.com/docs/getting-started/:

```bash
# Setup Environment
vagrant up

# Browse to sample website (optional)
open https://192.168.33.10

# Scan and evaluate configuration
git clone git@github.com:drwetter/testssl.sh.git
./testssl.sh/testssl.sh 192.168.33.10
```

## Questions?

Contact: Ian Lee <lee1001@llnl.gov>
