# SecuraX

SecuraX is an advanced cybersecurity toolkit designed to help organizations and individuals secure their digital infrastructure. It focuses on proactive threat detection and vulnerability management, providing essential tools for identifying and mitigating security risks across networks, systems, and applications.

## Features
- 🔍 Proactive threat detection
- 🛡️ Vulnerability scanning & analysis
- 📊 Log monitoring & anomaly detection
- ⚙️ Customizable security rules

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/SecuraX.git
   cd SecuraX
pip install -r requirements.txt
python src/detection.py --logfile /var/log/auth.log
python src/detection.py --logfile /var/log/auth.log
import re
import re
import logging

# Setup logging
logging.basicConfig(filename="threats.log", level=logging.INFO, format="%(asctime)s - %(message)s")

def analyze_log(file_path):
    failed_attempts = {}

    with open(file_path, "r") as log_file:
        for line in log_file:
            if "Failed password" in line:
                ip_match = re.search(r"(\d+\.\d+\.\d+\.\d+)", line)
                if ip_match:
                    ip_address = ip_match.group(0)
                    failed_attempts[ip_address] = failed_attempts.get(ip_address, 0) + 1

                    if failed_attempts[ip_address] > 5:  # Alert threshold
                        alert_msg = f"Possible brute force attack detected from {ip_address}!"
                        print(alert_msg)
                        logging.info(alert_msg)

if __name__ == "__main__":
    log_file_path = "/var/log/auth.log"  # Update as needed
    analyze_log(log_file_path)