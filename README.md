# 🚀 PocketMine-MP 0.14.x for ARM64 (Legacy Fixed)
Maintained by: **zxcvbnmz3-MCPE**

This repository provides a complete, pre-configured environment to run legacy **Minecraft: PE v0.14.x** servers on modern **ARM64** Android devices. It includes a custom-built PHP 7.2 binary and patched source code to ensure compatibility with modern Android systems.

---

## 🛠 Prerequisites
You must have **Termux** installed on your Android device (Android 7.0+ recommended).

## 📥 Full Installation & Setup Guide

### Step 1: Update Termux & Install Required Tools
```bash
pkg update && pkg upgrade -y
pkg install git tar -y
```

### Step 2: Clone the Repository
Download the entire project from GitHub to your local storage:
```bash
git clone [https://github.com/zxcvbnmz3-MCPE/PocketMine-0.14-ARM64-Fixed.git](https://github.com/zxcvbnmz3-MCPE/PocketMine-0.14-ARM64-Fixed.git)
```

### Step 3: Navigate into the Project Folder
Use the `cd` command to enter the repository directory:
```bash
cd PocketMine-0.14-ARM64-Fixed
```

### Step 4: Extract the System Files
The binaries and source code are compressed to preserve file permissions. Extract them using:
```bash
tar -xzvf php-binary.tar.gz
tar -xzvf server-files.tar.gz
```

### Step 5: Configure Global PHP (Crucial Step)
To use the `php` command globally without typing the full path every time, you must add it to your environment variables:
```bash
echo "export PATH=$PATH:$(pwd)/php-fast/bin" >> ~/.bashrc
source ~/.bashrc
```
*Verification: Type `php -v` to ensure it displays "PHP 7.2.34".*

### Step 6: Launch the Server
Now you are ready to start your Minecraft server:
```bash
php G-0.14/src/pocketmine/PocketMine.php
```

---

## 🔧 Technical Modifications Applied
This version has been surgically patched by **zxcvbnmz3-MCPE** to fix common "Legacy" errors:
1. **Keyword Conflict Fix**: Renamed the `Void` class to `VoidGenerator` (since `void` is a reserved keyword in PHP 7+).
2. **PHP 7.2 Compatibility**: Patched `src/pocketmine/level/Level.php` (line 3143) to handle `count()` warnings that previously crashed the console.
3. **Custom Build**: PHP 7.2.34 compiled with `pthreads` (v3.1.6) and `YAML` support for maximum performance on ARM64 mobile CPUs.

## 📢 Credits & Contribution
- **Developer**: zxcvbnmz3-MCPE
- **Original Engine**: Genisys / PocketMine-MP

---
*Keeping the 0.14.x legacy alive on modern hardware.*