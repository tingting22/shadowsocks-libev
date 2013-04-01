shadowsocks-libev
=================

[![Build Status](https://secure.travis-ci.org/madeye/gaeproxy.png)](http://travis-ci.org/madeye/shadowsocks-libev)

Intro
-----

[Shadowsocks-libev](http://shadowsocks.org) is a lightweight secured scoks5 
proxy for embedded devices and low end boxes.

It is a port of [shadowsocks](https://github.com/clowwindy/shadowsocks) 
created by [@clowwindy](https://github.com/clowwindy).

Features
--------

Shadowsocks-libev is writen in pure C and only depends on
[libev](http://software.schmorp.de/pkg/libev.html).

When statically linked and packaged for OpenWRT, the total package size is 23KB. 
In normal usage, the memory consumption is about 600KB and the CPU utilization is 
no more than 5% on a low-end router (Buffalo WHR-G300N V2 with a 400MHz MIPS CPU, 
32MB memory and 4MB flash).

Installation
------------

Build the binary like this:

```bash
    sudo apt-get install build-essential autoconf libtool libev-dev
    ./configure && make
```

Usage
-----

```
usage:

    ss-local -s server_host -p server_port -l local_port -k password
       [-m encrypt_method] [-f pid_file] [-t timeout] [-c config_file]

    ss-server -s server_host -p server_port -k password
       [-m encrypt_method] [-f pid_file] [-t timeout] [-c config_file]

options:

    encrypt_method:     table, rc4
          pid_file:     valid path to the pid file
           timeout:     socket timeout in senconds
       config_file:     json format config file

```
