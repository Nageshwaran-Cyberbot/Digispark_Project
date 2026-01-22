
# Digispark Security Toolkit

This project is a collection of security research and demonstration tools using the Arduino Digispark ATTiny85 microcontroller. Each tool is designed for educational, ethical hacking, and penetration testing purposes only. The scripts showcase how USB-based microcontrollers can be used for automation, security testing, and awareness.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Flashing Scripts](#flashing-scripts)
- [Folder & Script Descriptions](#folder--script-descriptions)
- [Ethical and Legal Notice](#ethical-and-legal-notice)
- [License](#license)

## Overview
This repository demonstrates various security concepts using the Digispark ATTiny85. The scripts automate tasks such as account creation, WiFi credential extraction, shell access, and more. These are intended for red team exercises, security awareness, and research.

## Project Structure

```
Digispark_Project/
├── Account_Creation/
├── Fork_Bomber/
├── Keylogger & DNS Poisoner/
├── Shell_Attacks/
├── Wifi_Attacks/
├── Windows_Jammer/
```


## How to Run the Source Codes

Each folder contains one or more `.ino` files (Arduino sketches) designed for the Digispark ATTiny85. To use any script:

### Prerequisites
- **Arduino IDE**: Download and install from [arduino.cc](https://www.arduino.cc/en/software)
- **Digispark Drivers**: Install Digispark drivers for your OS ([instructions here](https://digistump.com/wiki/digispark/tutorials/connecting))

### Flashing a Script to Digispark
1. Open Arduino IDE.
2. Go to **File > Open** and select the desired `.ino` file (e.g., `Account_Creation.ino`).
3. Go to **Tools > Board > Digispark (Default - 16.5mhz)**.
4. Click the **Upload** button (right arrow).
5. When prompted, insert your Digispark device into a USB port.
6. Wait for the upload to complete. The device is now programmed.

### Using the Programmed Digispark
1. Remove the Digispark from your computer.
2. Insert it into the target Windows machine.
3. The payload will execute automatically (no further action needed).

> **Note:** Some scripts may require the target machine to be unlocked and at the desktop. For WiFi attacks, see the comments in each `.ino` file for OS compatibility.

### Example: Flashing and Running `Account_Creation.ino`
1. Open `Account_Creation.ino` in Arduino IDE.
2. Select Digispark board.
3. Click Upload and insert Digispark when prompted.
4. Plug the Digispark into the target machine to create a new admin account automatically.

Repeat these steps for any other `.ino` file in the project.

---

## Folder & Script Descriptions

### Account_Creation
- **Account_Creation.ino**: Creates a new local admin user on Windows.
- **Account_Creation.md**: Documentation for the script.

### Fork_Bomber
- **Fork_Bomb.ino**: Launches a Windows fork bomb via command prompt.
- **Persistent_Fork_Bomb.ino**: Places a fork bomb in the Windows startup folder for persistence.
- **fork_bomber.md**: Details and removal tips.

### Keylogger & DNS Poisoner
- **DNS_Poisoner.ino**: Modifies Windows hosts file to redirect domains.
- **Κeylogger.ino**: (File present, content not summarized here.)

### Shell_Attacks
- **Rapid_Shell.ino, Reverse_Shell.ino, Powershell_Script.ino**: Various scripts for reverse/rapid shell access.
- **Invoke-PowerShellTcpOneLine.ps1**: PowerShell one-liner for reverse shell.
- **az_qw_convert.sh**: Utility script.
- **README.md, rapid_shell.md, reverse_shell.md**: Documentation.

### Wifi_Attacks
- **WiFi_Profile_Grabber.ino**: Extracts WiFi profiles.
- **WiFi_Profile_Mailer.ino, WiFi_Profile_Mailer_New.ino, Wifi_Profile_Mailer_Update.ino**: Extracts and emails WiFi credentials (see `wifi-profile.md` for OS compatibility).
- **wifi-profile.md**: Usage notes for each script.

### Windows_Jammer
- **Window_Jammer.ino**: Simulates input jamming/denial on Windows.
- **README.md**: Module documentation.

## Ethical and Legal Notice
This toolkit is for authorized security testing, research, and educational use only. Do not use these tools on systems you do not own or have explicit permission to test. Misuse may be illegal and unethical. The authors assume no responsibility for misuse or damages.

## License
See the [LICENSE](LICENSE) file for details.
