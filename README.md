# vialectrumx-installer
A script to automate the installation of vialectrumx 🤖

Installing vialectrumx isn't really straight-forward (yet). You have to install the latest version of Python and various dependencies for
one of the database engines. Then you have to integrate vialectrumx into your init system.

`vialectrumx-installer` simplifies this process to running a single command. All that's left to do for you
is to customise the configuration and to start vialectrumx

## Usage
This installs electrumx using the default options:

    wget https://raw.githubusercontent.com/vialectrum/vialectrumx-installer/master/bootstrap.sh -O - | bash

You can also set some options if you want more control:

| -d --dbdir | Set database directory (default: /db/) |
|------------|----------------------------------------|
| --update   | Update previously installed version    |
| --leveldb  | Use LevelDB instead of RocksDB         |

For example:

    wget https://raw.githubusercontent.com/vialectrum/vialectrumx-installer/master/bootstrap.sh -O - | bash -s - -d /media/ssd/electrum-db
     
## Operating System Compatibility

The following operating systems are officially supported and automatically being tested against:

| OS | Status |
|----------|---:|
| Debian Jessie  | [![debian](https://badges.herokuapp.com/travis/bauerj/electrumx-installer?env=IMAGE=%22debian:8%22&label=debian:8)](https://travis-ci.org/bauerj/electrumx-installer/) |
| Ubuntu 16.04   | [![ubuntu](https://badges.herokuapp.com/travis/bauerj/electrumx-installer?env=IMAGE=%22ubuntu:16.04%22&label=ubuntu:16.04)](https://travis-ci.org/bauerj/electrumx-installer/) |
| CentOS 7       | [![centos](https://badges.herokuapp.com/travis/bauerj/electrumx-installer?env=IMAGE=%22centos:7%22&label=centos:7)](https://travis-ci.org/bauerj/electrumx-installer/) |
| Debian Stretch | [![debian](https://badges.herokuapp.com/travis/bauerj/electrumx-installer?env=IMAGE=%22debian:9%22&label=debian:9)](https://travis-ci.org/bauerj/electrumx-installer/) |

