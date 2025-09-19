# Reconyx
# Reconyx - Domain Recon Tool

Reconyx is a **bash-based domain reconnaissance tool** designed for subdomain enumeration and discovery.
It automates collection from multiple sources, manages API key syncing, and provides options for verbose output and live subdomain checking.

---

## ✨ Features

* 🎨 **Colored ASCII Banner** with typing effect.
* 🔧 **Dependency auto-check & installer** for required tools.
* 🔑 **API key sync** (Subfinder, Chaos, Findomain).
* 🌐 **Subdomain enumeration** using:

  * [Subfinder](https://github.com/projectdiscovery/subfinder)
  * [Assetfinder](https://github.com/tomnomnom/assetfinder)
  * [Findomain](https://github.com/findomain/findomain)
  * [Chaos](https://github.com/projectdiscovery/chaos-client) (if API key set)
  * [crt.sh](https://crt.sh/)
* 📂 **Organized results** saved into per-domain folders.
* 🔍 **Verbose mode** (`-v`) to print results live with typing effect.
* 🟢 **Alive subdomain check** (`-a`) with [httpx](https://github.com/projectdiscovery/httpx) or fallback `curl`.
* 📝 Saves results into:

  * `domain/subdomains_domain.txt`
  * `domain/alive_subdomains_domain.txt` (if `-a` used)

---

## ⚙️ Installation

Clone the repo:

```bash
git clone https://github.com/fariaahmed13/Reconyx.git
cd Reconyx
chmod +x reconyx
```

Run the tool:

```bash
./reconyx -d example.com
```

---

## 📦 Dependencies

Reconyx installs/checks dependencies automatically, but it relies on:

* `curl`
* `jq`
* `subfinder`
* `assetfinder`
* `findomain`
* `chaos` (optional, requires API key)
* `httpx` (optional, for alive subdomain checking)

Make sure Go is installed for `subfinder`, `assetfinder`, and `chaos`:

```bash
sudo apt install golang -y
```

---

## 🔑 API Keys

For better results, set API keys in:

* `~/.config/subfinder/provider-config.yaml`
* `~/.config/chaos/config.yaml`
* `~/.findomain/config.json`

Reconyx will auto-detect and sync keys if present.

---

## 🚀 Usage

### Single Domain:

```bash
./reconyx -d target.com
```

### Domain List:

```bash
./reconyx -l domains.txt
```

### Verbose Mode (show subdomains live):

```bash
./reconyx -d target.com -v
```

### Alive Subdomains Only:

```bash
./reconyx -d target.com -a
```

### Combined:

```bash
./reconyx -l domains.txt -v -a
```

---

## 📂 Output Example

```
target.com/
 ├── subdomains_target.com.txt
 └── alive_subdomains_target.com.txt
```

---

## ⚠️ Disclaimer

This tool is for **educational and security research purposes only**.
Do not use it against systems without proper authorization.

---

## 👨‍💻 Author

**Faria Ahmed**
GitHub: [fariaahmed13](https://github.com/fariaahmed13)
