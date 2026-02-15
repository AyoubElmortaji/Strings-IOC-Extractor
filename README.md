# Strings-IOC-Extractor


A lightweight, **100% client-side** web app that parses the output of `strings` (from malware samples) and extracts common indicators:
- URLs / Domains / IPs (+ optional ports)
- HTTP methods & header hints
- Suspicious API calls (WinAPI + some POSIX/network)
- File paths (Windows + Linux)
- Registry keys
- Emails
- Base64 blobs (heuristic)

✅ Runs locally in your browser (no server).  
✅ Responsive UI with category tabs + search filter.  
✅ Export results as **JSON** or **CSV**.

> **Disclaimer**: This tool is for **educational and defensive security** use only. Always analyze malware in an isolated environment.

---

## Demo

1. Open the app
2. Click **Load demo**
3. Browse results by clicking category tabs (URLs, API Calls, IPs, etc.)

---

## Features

- **Category browsing**: click a tab to view only that category’s results
- **Search/filter** inside the current category  
  - Supports regex: `/http|c2/i`
- **Severity labels**: `OK / WARN / BAD` (simple triage heuristics)
- **Deduplication toggle**
- **Min string length slider**
- **Case-insensitive API detection** toggle
- **Export**
  - `ioc_results.json`
  - `ioc_results.csv`

---


```bash
strings -a sample.bin > file.txt
