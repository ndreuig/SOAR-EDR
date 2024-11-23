# Lima Charlie EDR Implementation
## Installation Documentation

### Prerequisites
- Kali Linux VM
- Internet connectivity
- Lima Charlie account
- Installation Key from Lima Charlie dashboard

### System Verification
Before installation, verify your system specifications:
```bash
# Check architecture
uname -m    # Should show x86_64
arch        # Should show x86_64

# Verify internet connectivity to Lima Charlie
curl -v https://limacharlie.io
telnet limacharlie.io 443
```
### Sensor Installation

```bash
# 1. Navigate to the directory where the downloaded .deb file is located.
cd /path/to/your/downloads

# 2. Install the LimaCharlie sensor
sudo dpkg -i limacharlie_4.31.1-1_amd64.deb

# 3. Enter your installation key
# This key is necessary for the sensor to connect to the LimaCharlie platform.

# 4. Successful Installation Check
dpkg -l | grep limacharlie

# 5. Service Status
sudo systemctl status limacharlie
```

# Testing Tools Setup
## LaZagne Password Recovery Tool

### Overview
LaZagne is a tool for recovering locally stored passwords.

**IMPORTANT**: Only use this tool ethically and legally with proper authorization.

### Installation Steps
1. Install Prerequisites
```bash
# Update package list and install requirements
sudo apt update
sudo apt install git python3
```
2. Clone Repository
```bash
# Get LaZagne from GitHub
git clone https://github.com/AlessandroZ/LaZagne.git
```
3. Setup and Execution
```bash
# Navigate to LaZagne directory
cd LaZagne
cd Linux

# Run LaZagne
python3 laZagne.py
```
