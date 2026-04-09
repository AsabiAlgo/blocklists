# Blocklists

Threat intelligence blocklists for the [Alparslan](https://github.com/Dijital-Savunma/alparslan) browser extension.

## USOM Blocklist

`usom-blocklist.txt` contains domains flagged by [USOM](https://www.usom.gov.tr/) (Turkish National CERT).

- **Domains**: ~465K
- **Format**: Newline-delimited, one domain per line
- **Version check**: `version.json` contains hash and count for efficient update checks

## Usage

The Alparslan extension fetches `version.json` first. If the hash has changed, it downloads the full list.

```
GET https://raw.githubusercontent.com/AsabiAlgo/blocklists/main/version.json
GET https://raw.githubusercontent.com/AsabiAlgo/blocklists/main/usom-blocklist.txt
```
