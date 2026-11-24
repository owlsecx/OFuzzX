# 🦉 OFuzzX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OFuzzX** — HTTP Parameter & Path Fuzzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OFuzzX — HTTP Parameter & Path Fuzzer. It provides target URL template with FUZZ marker in path, query, header value and request body; auto-detection of existing query parameters for one-by-one fuzzing. Operators can export results (including machine-readable formats) and gate CI with severity thresholds where supported.

---

## ✨ Features

- Target URL template with FUZZ marker in path, query, header value and request body; auto-detection of existing query parameters for one-by-one fuzzing.
- Embedded, compact wordlists: paths, params, XSS canaries, SSTI canaries, path-traversal, backup suffixes and API verbs — plus external file loading.
- Mutation engine: case folds, URL-encode, double URL-encode, unicode homoglyph/overlong tricks and a null-byte suffix — all opt-in, detection-only.
- Threaded urllib engine (ThreadPoolExecutor) with a token-bucket rate limiter, per-request timeout, redirect follow/no-follow, custom headers, cookies, method, body and an optional TLS-verify bypass.
- Response scoring: status, length, word/line counts, <title> extraction, reflection detection and error signature heuristics (stack traces, SQL errors, path disclosure) — read-only, nothing is exploited.
- Baseline calibration against a control request plus an interesting-hit filter that keeps only anomalies (status change, size delta %, new keywords, reflects).

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OFuzzX                                     # interactive menu
./OFuzzX --json -o report.json
./OFuzzX --url https://example.com
./OFuzzX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OFuzzX --help   # watch every network call
firejail --net=none ./OFuzzX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
