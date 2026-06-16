# Comodo ModSecurity Rules (CWAF) - Custom and Updated Version

This repository contains the original rule base of the Comodo Web Application Firewall (CWAF), independently maintained and enriched with frequent updates based on the [SBB-WAF-Rules](https://github.com/sminozzi/SBB-WAF-Rules) project.

The package features global optimizations to reduce false positives and support for custom rules, making it ideal for those who want to keep the Comodo ecosystem active and protected against new threats.

## 📁 Repository Structure

* `cwaf.conf`: Master file managing the ecosystem's loading order.
* `rules/`: Folder containing official rules (.conf) and data files (.data) powered by updated patches.
* `global/zzz_exclude_global.conf`: Mitigation file with globally disabled rules to prevent breaking common applications.
* `custom_user.conf`: File dedicated to your custom rules.
* `domains/`: Folder for domain-specific configurations and exceptions.

---

## 🚀 How to Install

### Prerequisites
* ModSecurity installed and active on the server (Apache, Nginx, or LiteSpeed).
* Root access or administrator privileges to edit web server configurations.

### Step 1: Download the rules
Clone this repository directly into your server's security directory (the default suggested path in the configuration is `/usr/local/apache/modsecurity-cwaf/`):

```bash
git clone [https://github.com/sminozzi/stopbadbots-comodo.git](https://github.com/sminozzi/stopbadbots-comodo.git) /usr/local/apache/modsecurity-cwaf/
