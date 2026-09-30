# Python VPS Server Monitoring via Discord Webhooks

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![Paramiko](https://img.shields.io/badge/Library-Paramiko-green.svg)](https://www.paramiko.org/)
[![License](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Discord](https://img.shields.io/badge/Discord-Bot-blueviolet.svg)](https://discord.com)

## 📋 Description

This **Server Monitor Bot** allows you to **monitor multiple VPS servers** in real-time through **Discord webhooks**. The bot collects system metrics like **CPU usage, RAM, Disk, and Network speeds** and sends them periodically to a designated **Discord channel**.

The bot uses **Paramiko SSH** to connect with multiple VPSs and provides updates with **real-time network traffic and all-time traffic statistics**. You can customize the bot with **server names, IPs**, and delay intervals using `.env` configuration.

---

## 🎯 Features

- **Real-Time Monitoring**: CPU, RAM, Disk usage, and network speeds.
- **All-Time Network Usage**: Tracks total IN and OUT network traffic.
- **ANSI Colored Output**: Beautifully formatted Discord messages using ANSI escape codes.
- **Supports Multiple VPS Servers**: Easily configurable with `.env` file.
- **Automatic Updates on Discord** via Webhook.

---

## 🛠️ Requirements

- **Python 3.9+**
- **Paramiko** library for SSH communication
- **requests** library for sending HTTP requests to Discord Webhooks
- **dotenv** to handle environment variables

Install required libraries via:
```bash
pip install paramiko requests python-dotenv
```

---

## 📁 Project Structure

```
server-monitor/
│
├── main.py                 # Main script to run the bot
├── .env                    # Environment variables (for credentials & config)
├── requirements.txt        # Dependencies
└── README.md               # Documentation (this file)
```

---

## ⚙️ Setup & Configuration

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/ChalanaGimhanaX/Server-Monitor-Via-Discord.git
   cd Server-Monitor-Via-Discord
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Create a `.env` File:**

   In the root directory, create a `.env` file with the following content:

   ```
   VPS_NAMES=Server1,Server2  # Comma-separated server names
   VPS_IPS=192.168.0.1,192.168.0.2  # Comma-separated VPS IPs
   VPS_USERS=root,admin  # SSH users
   VPS_PASSWORDS=password1,password2  # SSH passwords
   WEBHOOK_URL=https://discord.com/api/webhooks/your-webhook-id  # Discord webhook URL
   DELAY=5  # Interval between updates (in seconds)
   ```

4. **Run the Bot:**
   ```bash
   python main.py
   ```

---

## 📌 Usage

Once the bot is running, it will send updates to the specified Discord channel every few seconds (based on the `DELAY` value). It will display:

- Server uptime and OS information
- CPU usage (with per-core stats)
- RAM and Disk usage
- Real-time and all-time network traffic

---
![Preview](https://github.com/user-attachments/assets/21dbb0f0-c9c7-41e4-bcdc-c87eb0e73feb)

## 🛡️ License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.
