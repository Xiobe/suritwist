# suritwist
Suritwist - Generating potential phishing domains lists for suricata alerting.

## Basic idea

The basic idea is that you generate your dnstwist domain variations for your domain of interest either [offline](https://github.com/elceef/dnstwist) or [online](https://dnstwist.it/) and export it into a JSON format.
You feed this JSON file into suritwist.py and it will generate you a base64 encoded list for these domains which can then be used in a rule for generating alerts for potential phishing.

## Usage

```shell
usage: suritwist [-h] [-e [EXCLUDE ...]] [-r] [--sid SID] [--rev REV] [-v] inputfile outputfile

Generate your dataset for dnstwist

positional arguments:
  inputfile             input file in json format
  outputfile            suricata dataset file

options:
  -h, --help            show this help message and exit
  -e [EXCLUDE ...], --exclude [EXCLUDE ...]
                        domains you want to exclude from the dataset
  -r, --rule            show rule
  --sid SID             specify your suricata rule id, default is 100001
  --rev REV             specify your revision, default is 1
  -v, --verbose         output verbose
```

## Dockerized dnstwist

You can find a dockerized version of dnstwist in our github repo [docker-dnstwist](https://github.com/theshellcompany/docker-dnstwist).
