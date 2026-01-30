# Trivy Security Scanner 🚀

A simple, powerful vulnerability and misconfiguration scanner for **Docker images**, **filesystems**, **Git repos**, and **Kubernetes clusters** — using the open-source tool Trivy by Aqua Security. :contentReference[oaicite:0]{index=0}

---

## 📌 Table of Contents

- 🔧 Installation  
- 📦 Usage  
- 💻 Commands  
- 📊 Example Outputs  
- 💡 GitHub CI/CD Integration  
- 📦 Contributing  
- 📄 License

---

## 🔧 Installation

You can install Trivy on Ubuntu/Debian using the official repository:

```bash
sudo apt-get install wget apt-transport-https gnupg lsb-release
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null
echo "deb [signed-by=/usr/share/keyrings/trivy.gpg] https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main" | sudo tee -a /etc/apt/sources.list.d/trivy.list
sudo apt-get update
sudo apt-get install trivy

---COMMANDS---

trivy image imagename

trivy fs --security-checks vuln,config   Folder_name_OR_Path

trivy image --severity HIGH,CRITICAL image_name

trivy image -f json -o results.json image_name

trivy repo repo-url

trivy k8s --report summary cluster   ```
