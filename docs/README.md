## Sewer          

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/ccf655afb3974e9698025cbb65949aa2)](https://www.codacy.com/app/komuW/sewer?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=komuW/sewer&amp;utm_campaign=Badge_Grade)
[![CircleCI](https://circleci.com/gh/komuw/sewer.svg?style=svg)](https://circleci.com/gh/komuw/sewer)
[![codecov](https://codecov.io/gh/komuW/sewer/branch/master/graph/badge.svg)](https://codecov.io/gh/komuW/sewer)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/komuw/sewer)


Sewer is a Let's Encrypt(ACME) client.  
It's name is derived from Kenyan hip hop artiste, Kitu Sewer.  

The current release is [0.8.2](https://komuw.github.io/sewer/0.8.2-notes).
You can see notes for the forthcoming [0.8.3](https://komuw.github.io/sewer/0.8.3-notes)
release.
There is also the [CHANGELOG](https://github.com/komuw/sewer/blob/master/CHANGELOG.md).
_(These should all be integrated soon as part of the move to Pages.)_

## Features
- Obtain or renew SSL/TLS certificates from [Let's Encrypt](https://letsencrypt.org)
- Supports acme version 2 (current RFC including post-as-get).
- Support for SAN certificates.
- Supports [wildcard certificates](https://komuw.github.io/sewer/wildcards).
- Bundling certificates.
- Supports [DNS and HTTP](https://komuw.github.io/sewer/UnifiedProvider) challenges
  - List of currently supported
    [DNS services and BYO-service notes](https://komuw.github.io/sewer/dns-01)
  - HTTP challenges are a new feature, no operational drivers in the tree
    yet.  [See usage and BYO-service notes](https://komuw.github.io/sewer/http-01)
- sewer is both a [command-line program](https://komuw.github.io/sewer/sewer-cli)
  and a [Python library](#usage) for custom use
- Well written(if I have to say so myself):
  - [Good test coverage](https://codecov.io/gh/komuW/sewer)
  - [Passing continous integration](https://circleci.com/gh/komuW/sewer)
  - [High grade statically analyzed code](https://www.codacy.com/app/komuW/sewer/dashboard)
  - type hinting to support mypy verification is a recently begun WIP

## Installation

```shell
pip3 install sewer

# with All DNS Provider support, include aliyun, Hurricane Electric, Aurora, ACME ...
# pip3 install sewer[alldns]

# with Cloudflare support
# pip3 install sewer[cloudflare]

# with Aliyun support
# pip3 install sewer[aliyun]

# with HE DNS(Hurricane Electric DNS) support
# pip3 install sewer[hurricane]

# with Aurora DNS Support
# pip3 install sewer[aurora]

# with ACME DNS Support
# pip3 install sewer[acmedns]

# with Rackspace DNS Support
# pip3 install sewer[rackspace]

# with DNSPod DNS Support
# pip3 install sewer[dnspod]

# with DuckDNS DNS Support
# pip3 install sewer[duckdns]

# with ClouDNS DNS Support
# pip3 install sewer[cloudns]

# with AWS Route 53 DNS Support
# pip3 install sewer[route53]

# with PowerDNS DNS Support
# pip3 install sewer[powerdns]
```

sewer(since version 0.5.0) is now python3 only. To install the (now unsupported) python2 version, run;

```shell
pip install sewer==0.3.0
```
Sewer is in active development and it's API ~~may~~ will change in backward incompatible ways.
[https://pypi.python.org/pypi/sewer](https://pypi.python.org/pypi/sewer)


## Development setup

See the how to contribute [documentation](https://github.com/komuw/sewer/blob/master/.github/CONTRIBUTING.md)

## TODO
- docs (WIP)
- support more DNS providers
- https://github.com/komuw/sewer/milestone/1

## FAQ
- Why another ACME client?          
  I wanted an ACME client that I could use to programmatically(as a library) acquire/get certificates. However I could not 
  find anything satisfactory for use in Python code.
- Why is it called Sewer?
  I really like the Kenyan hip hop artiste going by the name of Kitu Sewer.                            