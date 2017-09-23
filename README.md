FastDNS Hook
============

This repository contains a python-based hook for [dehydrated][0] that allows
a user to obtain a certificate from the [Let's Encrypt][1] API via the `dns-01`
challenge. This hook, given the correct credentials, will automatically add
the challenge `TXT` record to your Akamai FastDNS configuration.

[0]: https://github.com/lukas2511/dehydrated/blob/master/dehydrated
[1]: https://letsencrypt.org/

## Installation

This script requires Python 2.7 (though converting it to Python 3 shouldn't be
difficult.) In addition, it requires:

 * dnspython
 * requests
 * edgegrid-python

All of which can be installed with pip:

```bash
$ pip install -r requirements.txt
```
