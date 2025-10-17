

Reconyx

⚡ Fast & Automated Domain Reconnaissance Tool

Reconyx is a **bash-based subdomain enumeration and reconnaissance tool** that combines results from multiple third-party utilities and passive sources. It supports API key integration, provides flexible verbose output, and can automatically identify live subdomains.

It is designed for **penetration testers, bug bounty hunters, and security researchers** who need quick, reliable, and well-organized domain reconnaissance.


---

🚀 Features

<img width="1356" height="810" alt="image" src="https://github.com/user-attachments/assets/271b6913-f6c7-4600-99a2-74612b514640" /># Reconyx

* 🎨 Clean ASCII banner with typing effect
* 🔧 Automatic dependency check & installation
* 🔑 API key syncing from existing configs (Subfinder, Chaos, Findomain)
* 🌐 Subdomain discovery via:

  * [Subfinder](https://github.com/projectdiscovery/subfinder)
  * [Assetfinder](https://github.com/tomnomnom/assetfinder)
  * [Findomain](https://github.com/findomain/findomain)
  * [Chaos](https://github.com/projectdiscovery/chaos-client)
  * [crt.sh](https://crt.sh/)
* 📂 Organized results: separate folder per target
* 📝 Output files:

  * `subdomains_target.txt`
  * `alive_subdomains_target.txt` (with `-a`)
* 🔍 Optional flags:

  * `-v` → Verbose (show subdomains live)
  * `-a` → Alive subdomain detection (using [httpx](https://github.com/projectdiscovery/httpx) or fallback `curl`)

---

## ⚙️ Installation

Clone the repo and make the script executable:

```bash
git clone https://github.com/fariaahmed13/Reconyx.git
cd Reconyx
chmod +x reconyx
```

Reconyx auto-checks and installs required dependencies, but ensure you have **Go** installed (for Subfinder, Assetfinder, Chaos):

```bash
sudo apt update && sudo apt install golang -y
```

---

## 🔑 API Setup

Some sources require API keys for maximum results.
Add your keys to these configs:

* **Subfinder:** `~/.config/subfinder/provider-config.yaml`
* **Chaos:** `~/.config/chaos/config.yaml`
* **Findomain:** `~/.findomain/config.json`

Reconyx will automatically detect and sync available keys.

---

## 📦 Dependencies

* `curl`
* `jq`
* `subfinder`
* `assetfinder`
* `findomain`
* `chaos` (optional, needs API key)
* `httpx` (optional, for alive subdomain check)

---

## 🛠️ Usage

### Single Domain

```bash
./reconyx -d example.com
```

### Multiple Domains (list)

```bash
./reconyx -l domains.txt
```

### Verbose Mode (show subdomains live)

```bash
./reconyx -d example.com -v
```

### Save Alive Subdomains

```bash
./reconyx -d example.com -a
```

### Combined Options

```bash
./reconyx -l domains.txt -v -a
```

---

📂 Output Structure

```
example.com/
 ├── subdomains_example.com.txt
 └── alive_subdomains_example.com.txt
```

---

⚠️ Disclaimer

This tool is intended for **educational and authorized security testing purposes only**.
Do not use Reconyx against targets you don’t own or have explicit permission to test.

---

👨‍💻 Author

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/fariaahmedmeem/)

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/fariaahmed13)

[![Gmail](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:contact.fariaahmed@gmail.com)

