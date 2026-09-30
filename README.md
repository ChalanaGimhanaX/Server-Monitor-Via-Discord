# Server Monitor via Discord

Python monitoring script that connects to VPS servers over SSH, collects system metrics, and sends formatted updates to a Discord webhook.

## Features

- Monitor multiple VPS instances from one script
- Collect CPU, memory, disk, uptime, OS, and network-traffic data
- Send periodic status updates to Discord through a webhook
- Configure server names, IPs, users, passwords, webhook URL, and delay from `.env`

## Requirements

- Python 3.9+
- SSH access to the target servers
- Discord webhook URL

Install dependencies:

```bash
pip install paramiko requests python-dotenv
```

## Configuration

Create a `.env` file:

```properties
VPS_NAMES=Server1,Server2
VPS_IPS=203.0.113.10,203.0.113.11
VPS_USERS=root,admin
VPS_PASSWORDS=password1,password2
WEBHOOK_URL=https://discord.com/api/webhooks/your-webhook-id
DELAY=5
```

Do not commit real server credentials or webhook URLs.

## Running

```bash
python main.py
```

The script will post updated server metrics to the configured Discord channel on the configured interval.

## Notes

This is a lightweight operations utility. Use private channels, restricted server credentials, and reasonable polling intervals.
