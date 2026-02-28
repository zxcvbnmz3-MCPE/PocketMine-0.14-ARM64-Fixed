# PocketMine-MP 0.14.x for ARM64 (Fixed & Patched)
Maintained by: **zxcvbnmz3-MCPE**

This repository provides a complete environment to run legacy **Minecraft: PE v0.14.x** servers on modern **ARM64** Android devices.

## 🛠 Prerequisites
You must have **Termux** installed.

## 📥 Setup Guide

### 1. Update & Install Tools
```bash
pkg update && pkg upgrade -y
pkg install git tar -y
```

### 2. Extract Files
```bash
tar -xzvf php-binary.tar.gz
tar -xzvf server-files.tar.gz
```

### 3. Make PHP Global
```bash
echo "export PATH=$PATH:$(pwd)/php-fast/bin" >> ~/.bashrc
source ~/.bashrc
```

### 4. Launch
```bash
php G-0.14/src/pocketmine/PocketMine.php
```

---
*Created by zxcvbnmz3-MCPE*