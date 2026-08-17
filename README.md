# 🔍 Subdomain Enumerator

[![Python Version](https://img.shields.io/badge/python-3.6+-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

A powerful, multi-threaded subdomain enumeration tool written in Python. Find all subdomains of a target domain using DNS resolution and HTTP checks.

---

## 🎯 What It Does

A **subdomain enumerator** finds all the subdomains associated with a target domain.


### Why This Matters

| Use Case | Explanation |
|----------|-------------|
| **🔐 Security Research** | Discover attack surfaces and hidden services |
| **🔎 OSINT** | Gather public information about a target |
| **🐛 Bug Bounty** | Find subdomains for vulnerability testing |
| **🛡️ Defensive Security** | Identify unauthorized or forgotten services |
| **📊 Asset Discovery** | Know what you own and need to protect |

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| **🚀 Multi-threaded** | Fast scanning using concurrent threads |
| **🌐 DNS Resolution** | Checks if subdomains actually exist |
| **🌍 HTTP/HTTPS Detection** | Identifies if subdomains have websites |
| **📝 Custom Wordlist Support** | Use your own subdomain list |
| **💻 Command-Line Interface** | Professional tool design |
| **💾 Results Saving** | Automatically saves findings to a file |
| **🛡️ Error Handling** | Graceful handling of DNS failures |
| **📊 Clean Output** | Easy-to-read results with indicators |

---

## 🧠 How It Works

### The Process
Load wordlist (list of common subdomain names)
├── www
├── mail
├── admin
└── 45+ more...

For each subdomain, build the full domain
├── www.example.com
├── mail.example.com
└── admin.example.com

Try to resolve each domain to an IP
├── www.example.com → 93.184.216.34 ✅ EXISTS
├── mail.example.com → 93.184.216.35 ✅ EXISTS
└── admin.example.com → ERROR ❌ DOESN'T EXIST

Check if resolved domains have websites
├── www.example.com → HTTP → 200 (OK)
└── mail.example.com → No HTTP

Print and save results
└── [+] www.example.com → 93.184.216.34 (http:// → 200)
