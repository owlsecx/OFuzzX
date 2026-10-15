# 🦉 OFuzzX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OFuzzX** — HTTP Parameter & Path Fuzzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

HTTP parameter & path fuzzer — template fuzzing with anomaly scoring

---

## ✨ Features

- Target URL template with FUZZ marker in path, query, header value and request body; auto-detection of existing query parameters for one-by-one fuzzing.
- Embedded, compact wordlists: paths, params, XSS canaries, SSTI canaries, path-traversal, backup suffixes and API verbs — plus external file loading.
- Mutation engine: case folds, URL-encode, double URL-encode, unicode homoglyph/overlong tricks and a null-byte suffix — all opt-in, detection-only.
- Threaded urllib engine (ThreadPoolExecutor) with a token-bucket rate limiter, per-request timeout, redirect follow/no-follow, custom headers, cookies, method, body and an optional TLS-verify bypass.
- Response scoring: status, length, word/line counts, <title> extraction, reflection detection and error signature heuristics (stack traces, SQL errors, path disclosure) — read-only, nothing is exploited.
- Baseline calibration against a control request plus an interesting-hit filter that keeps only anomalies (status change, size delta %, new keywords, reflects).
- Depth-limited recursion into discovered directories.
- Live result table and TXT / CSV / JSON export with a location chooser; clipboard copy of hit URLs.
- Full CLI (-u -w -H -X --marker --threads --json --version) alongside the interactive menu.
- Settings persisted to ~/OFuzzX/config.json.

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OFuzzX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
