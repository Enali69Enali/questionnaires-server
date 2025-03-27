# Setting Up a Raspberry Pi Environment

This guide walks you through setting up a Raspberry Pi environment with Python and Flask.

---

## Start to Create the Same Environment

### 1. Purchase a Raspberry Pi
Buy a Raspberry Pi from [Amazon](https://www.amazon.fr/dp/B0D1N3V2FF?ref=ppx_yo2ov_dt_b_fed_asin_title).

### 2. Download the 64-bit Image for MPU
Download the official 64-bit Raspberry Pi OS image from:
[Download Link](https://downloads.raspberrypi.com/raspios_full_arm64/images/raspios_full_arm64-2024-11-19/2024-11-19-raspios-bookworm-arm64-full.img.xz)

### 3. Flash the Image
- Use software like **Raspberry Pi Imager** or **balenaEtcher** to flash the image onto a microSD card.
- You will need a **mouse and a keyboard** for initial setup.

### 4. Configure the Raspberry Pi
1. Set up a profile.
2. Connect to **WiFi**.
3. Wait for the installation to complete.

---

## Enable SSH for Remote Access

### 1. Open a Terminal
```bash
sudo systemctl status ssh
```
If SSH is not running, start it with:
```bash
sudo systemctl start ssh
```

### 2. Find Your Raspberry Pi's IP Address
```bash
hostname -I
```
Example output: `192.168.1.29`

---

## Install Python and Flask Server

### 1. Install Python and Pip
```bash
sudo apt install python3 python3-pip -y
```

### 2. Install Flask and SQLAlchemy
```bash
pip3 install flask flask-sqlalchemy
```

### 3. Set Up a Virtual Environment
```bash
source flask_env/bin/activate
```

### 4. Run Your Flask Application
```bash
python3 app.py
```

Your Flask server should now be running!
