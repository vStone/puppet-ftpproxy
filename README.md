# Puppet FTP-Proxy

## Requirements

* [concat module](https://github.com/ripienaar/puppet-concat)

## Tested on...

* Debian 6 (Squeeze)
* Debian 7 (Wheezy)

## Example usage

### Install FTP-Proxy

    node /box/ {
      include ftpproxy
    }

### Adjust FTP-Proxy settings

    node /box/ {
      class { 'ftpproxy':
        listen_address => '0.0.0.0',
        listen_port    => '21',
      }
    }

### Chrooted FTP-Proxy

    node /box/ {
      class { 'ftpproxy':
        chroot_dir    => '/var/lib/ftp-proxy',
        chroot_enable => true,
      }
    }

### Add per user configuration

    ftpproxy::user { 'user1':
      ensure   => present,
      time_out => '90',
    }

    ftpproxy::user { 'user2':
      ensure       => present,
      time_out     => '90',
      same_address => true,
    }

