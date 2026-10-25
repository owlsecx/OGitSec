# 🦉 OGitSec

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OGitSec** — Git Repository Secret & History Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OGitSec — Git Repository Secret & History Auditor. It provides working-tree scanner — walks any repo or directory, optional .gitignore awareness (git ls-files or a built-in fnmatch fallback), binary & size guards. Operators can export results (including machine-readable formats) and gate CI with severity thresholds where supported.

---

## ✨ Features

- Working-tree scanner — walks any repo or directory, optional .gitignore awareness (git ls-files or a built-in fnmatch fallback), binary & size guards
- 70+ secret rules — AWS, GCP, Azure, GitHub, GitLab, Slack, Stripe, Twilio, SendGrid, npm, PyPI, Docker, PEM private keys, JWTs, URL credentials, basic auth
- Shannon entropy engine for generic assignments (base64 / hex alphabets, per-alphabet thresholds)
- History scanner — git log -p over all refs with commit / author / date / path attribution, depth cap and subprocess timeouts
- Diff scanner — staged (--cached) and unstaged changes for pre-commit and CI gating (--fail-on SEVERITY)
- False-positive heuristics — placeholders, examples, repeated chars, all-zeros, test fixtures, inline `ogitsec:allow` pragmas, allowlist / denylist files

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OGitSec                                     # interactive menu
./OGitSec --path ./config_or_ruleset
./OGitSec --json -o report.json
./OGitSec --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
