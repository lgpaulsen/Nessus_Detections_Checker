# Nessus Detections Checker

A small CLI tool that scrapes [Tenable's CVE pages](https://www.tenable.com/cve/) and lists the Nessus plugins that detect a given CVE.

For a CVE ID, it fetches the plugin table from `https://www.tenable.com/cve/<CVE-ID>/plugins` and prints each plugin's ID, name, family, severity, and URL.

## Install

```sh
pip install -r requirements.txt
```

## Usage

```sh
python nessus_detections.py CVE-2025-20828
python nessus_detections.py CVE-2025-20828 --output json
```

### Arguments

- `cve_id` — CVE identifier (e.g. `CVE-2025-20828`)
- `--output {text,json}` — output format (default: `text`)
