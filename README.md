# **USB Data Collector -- Automated Backup Tool**

[![Version](https://img.shields.io/badge/version-2.2-blue.svg)]()
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Built by Nuknov](https://img.shields.io/badge/Built%20by-Nuknov-000000?logo=github&logoColor=white)](https://github.com/Nuknov)
[![Red Team Research](https://img.shields.io/badge/Red%20Team%20Research-Nuknov-8B0000?logo=terminal)](https://nuknov.github.io)

**USB Data Collector** is a lightweight Windows automation tool that automatically copies selected user folders to a USB drive.

Perfect for **authorized backups, system administration tasks, and red team lab simulations** in a controlled environment.

**Windows Only. Silent. Efficient.**  
Built for **red team researchers, system administrators, and security professionals** who need automated data collection capabilities.

---

## 🧩 **What USB Data Collector Does**

- Automatically detects **USB drive letter** (E:, D:, etc.)
- Silently copies **multiple user folders** to USB
- Creates a **hidden destination folder** (`CollectedData`)
- Runs **without console window** for stealth
- Fully **customizable** folder selection
- Operates **entirely locally** with no network activity

Designed for **authorized testing, backups, and research in controlled environments**.

> \* *This tool requires explicit permission before use. See disclaimer below.*

---

## 🛰️ **Tech Stack**

- **Windows Batch Script** – Native Windows automation
- **Silent Execution** – No visible console windows
- **Robocopy Integration** – Efficient file copying
- **Auto USB Detection** – Dynamic drive letter recognition
- **Hidden Folders** – Discreet data storage

---

## ⚡ **Features**

| Feature                     | Details                                                     |
|----------------------------|-------------------------------------------------------------|
| Auto USB Detection         | Automatically finds USB drive letter                        |
| Multi-Folder Backup        | Collects Documents, Pictures, Videos, Favorites             |
| Silent Execution           | Runs without displaying console windows                     |
| Hidden Destination         | Creates hidden `CollectedData` folder on USB                |
| Customizable               | Easily add or remove target folders                         |
| No External Dependencies   | Pure batch script, no additional software needed            |
| Lightweight                | Minimal footprint, runs on any Windows system               |

---

## 🛠️ Installation

### Quick Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Nuknov/USB-Data-Collector.git
   cd USB-Data-Collector
   ```

2. **Copy to your USB drive**
   - Copy the entire folder to your USB drive root

3. **Run the tool**
   - Double-click `launch.bat` on the USB drive
   - The script will automatically:
     - Detect the USB drive letter
     - Create a hidden `CollectedData` folder
     - Begin copying selected folders

4. **Wait for completion**
   - Process time depends on data size
   - Large folders (GBs) may take several minutes

---

## 📂 **Default Backup Folders**

The tool collects these user folders by default:

- **Documents** – `%USERPROFILE%\Documents`
- **Favorites** – `%USERPROFILE%\Favorites`
- **Pictures** – `%USERPROFILE%\Pictures`
- **Videos** – `%USERPROFILE%\Videos`

---

## ⚙️ How It Works

USB Data Collector uses **native Windows batch scripting** to:

1. **Detect USB drive letter** automatically when script runs
2. **Create hidden folder** named `CollectedData` on USB
3. **Use robocopy** to efficiently copy user folders
4. **Run silently** without showing console windows
5. **Complete automatically** without user interaction

### Example Command Structure

```bat
%backupcmd% "%USERPROFILE%\Pictures" "%dest%\Pictures"
```

✅ **Runs entirely locally**  
✅ **No network activity**  
✅ **Fully open source**

---

## 🔧 **Customization**

### Adding More Folders

Edit the batch script to include additional folders:

```bat
%backupcmd% "%USERPROFILE%\Desktop" "%dest%\Desktop"
%backupcmd% "%USERPROFILE%\Downloads" "%dest%\Downloads"
%backupcmd% "%APPDATA%\Mozilla" "%dest%\Mozilla"
```

### Changing Destination Folder Name

Modify the `dest` variable in the script:

```bat
set "dest=%USB_DRIVE%\MyBackup"
```

---

## ⚠️ **Disclaimer**

> **IMPORTANT: This tool is for educational and authorized testing purposes ONLY.**
>
> - You **MUST** have **explicit permission** from the system owner before use
> - This tool is designed for **controlled lab environments** and **authorized backup scenarios**
> - The author is **NOT responsible** for any misuse or unauthorized use
>
> **Detection Risk:**  
> - Detection probability is approximately **50/50** depending on environment
> - Large data transfers (gigabytes) take time and increase detection risk
> - **Kaspersky antivirus can now detect this tool**
>
> **Recommendations:**  
> - **Modify the script** to match your specific use case
> - Test in **controlled lab environments** first
> - Ensure you have **written authorization** before deployment
>
> Always comply with applicable laws and ethical guidelines.

---

## 🧠 **Use Cases**

- **Authorized security assessments** in red team engagements
- **System administration backups** with proper authorization
- **Research and education** in controlled cybersecurity labs
- **Personal backup automation** for your own systems
- **Penetration testing training** in legal environments
- **Data recovery** from authorized systems

Ideal for **security researchers** who need efficient data collection in authorized scenarios.

---

## 🛡️ **Detection & Evasion Notes**

- **Antivirus Detection:** Kaspersky and other modern AV solutions may flag this
- **Process Time:** Large datasets increase exposure time
- **Behavioral Analysis:** Silent execution may trigger heuristic detection
- **Recommendations:**
  - Use only in **authorized environments**
  - Modify script signatures for **research purposes**
  - Test in **isolated lab networks** first
  - Consider **file size limits** to reduce transfer time

---

## 📋 **Requirements**

- **Windows OS** (7, 8, 10, 11)
- **USB Drive** with sufficient storage space
- **Administrator privileges** may be required for some folders
- **Robocopy** (included in Windows by default)

---

## 🔗 **Links**

- **GitHub:** [github.com/Nuknov](https://github.com/Nuknov)
- **Portfolio:** [nuknov.github.io](https://nuknov.github.io)
- **Report Issues:** [GitHub Issues](https://github.com/Nuknov/USB-Data-Collector/issues)

---

## **Author**

**Created by:** [Nuknov](https://github.com/Nuknov)

---

## ⭐ **Support**

If you find this project useful for your security research, please consider:
- ⭐ **Starring** the repository
- 🐛 **Reporting bugs** via GitHub Issues
- 🤝 **Contributing** improvements
- 📢 **Sharing** with the security research community

---

*Remember: With great power comes great responsibility. Use ethically. Always get permission.*
