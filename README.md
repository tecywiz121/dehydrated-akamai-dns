FastDNS Hook
============

This repository contains a python-based hook for [`letsencrypt.sh`][0]. That
allows a user to obtain a certificate from the [Let's Encrypt][1] API via the
`dns-01` challenge. This hook, given the correct credentials, will automatically
add the challenge `TXT` record to your Akamai FastDNS configuration.

[0]: https://github.com/lukas2511/letsencrypt.sh
[1]: https://letsencrypt.org/

## Installation

This script requires Python 2.7 (though converting it to Python 3 shouldn't be
difficult.) In addition, it requires:

 * dnspython
 * requests
 * edgegrid-python

All of which can be installed with pip:

```bash
$ pip install dnspython requests edgegrid-python
```

Then clone the files required for installation:

```bash
$ git clone https://github.com/lukas2511/letsencrypt.sh.git
$ git clone https://github.com/tecywiz121/letsencrypt-akamai-dns.git letsencrypt.sh/hooks/fastdns
```

## Configuration

Edit the script, and insert your Akamai credentials in the proper constants.

## Usage

```bash
$ cd letsencrypt.sh
$ ./letsencrypt.sh -c -t dns-01 -d example.com -k ./hooks/fastdns/fastdns_hook
```
