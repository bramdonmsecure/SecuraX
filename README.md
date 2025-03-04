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
    failed_attempts = {}import re
import logging

# Configure logging to store threat logs
logging.basicConfig(filename="threats.log",
                    level=logging.INFO,
                    format="%(asctime)s - %(message)s")

def analyze_log(file_path):
    failed_attempts = {}
import re
import logging

# Configure logging
logging.basicConfig(filename='security.log', level=logging.INFO, format='%(asctime)s - %(message)s')

def analyze_log(file_path):
    failed_attempts = {}

import re
import logging

# Configure logging
logging.basicConfig(filename='security.log', level=logging.INFO, format='%(asctime)s - %(message)s')

def analyze_log(file_path):
    failed_attempts = {}
import re
import logging

# Configure logging
logging.basicConfig(filename='security.log', level=logging.INFO, format='%(asctime)s - %(message)s')
def analyze_log(file_path):
    failed_attempts = {}

try:
with open(file_path, "r") as log_file:
for line in log_file:
if "Failed password" in line:
ip_match = re.search(r"\d+\.\d+\.\d+\.\d+", line)
if ip_match:
ip_address = ip_match.group(0)
failed_attempts[ip_address] = failed_attempts.get(ip_address, 0) + 1

# Set an alert threshold (e.g., more than 5 failed attempts)
if failed_attempts[ip_address] > 5:
alert_msg = f"Possible brute-force attack detected from IP: {ip_address}"
print(alert_msg)
logging.info(alert_msg)
except FileNotFoundError:
print(f"Error: The file {file_path} was not found. Check the file path and permissions.")
except Exception as e:
print(f"An error occurred: {e}")
if __name__ == "__main__":
log_file_path = "/var/log/auth.log"  # Ensure this path is correct for your system