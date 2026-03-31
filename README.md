# SysMon — System Monitoring OpenClaw Skill

> Full-stack system monitoring skill for OpenClaw agents.
> CPU, RAM, disk, network, processes, temperature, automated alerts, and health reports.

---

## What This Skill Does

| Module | Description |
|---|---|
| 🔥 CPU Monitoring | Per-core usage, load avg, temperature, top processes |
| 🧠 Memory Monitoring | RAM breakdown, swap, memory leak detection |
| 💾 Disk Monitoring | Space analysis, I/O stats, SMART health, inode usage |
| 🌐 Network Monitoring | Bandwidth per interface, active connections, DNS traffic |
| ⚙️ Process Management | Process tree, kill by name, zombie detection, port listeners |
| 🚨 Automated Alerts | Threshold alerts for CPU/RAM/disk — extensible to Telegram/email |
| 📊 Health Reports | Full JSON system snapshot saved to disk |
| 🪟 Windows Support | PowerShell equivalents for all major commands |

---

## Installation

### Load into OpenClaw

```bash
cp SKILL.md ~/.hermes/skills/productivity/sysmon/SKILL.md
```

### Install Dependencies

```bash
pip install psutil
sudo apt install -y sysstat net-tools nethogs ifstat smartmontools lm-sensors
```

---

## Usage Examples

Once loaded, trigger the skill with natural language:

- *"Why is my CPU so high?"*
- *"What's eating all my RAM?"*
- *"How much disk space do I have left?"*
- *"Show me all network connections"*
- *"Generate a full system health report"*
- *"Alert me if CPU goes above 90%"*
- *"Find the top 10 memory-hungry processes"*

---

## Requirements

- Python 3.x + `psutil`
- Linux: `sysstat`, `net-tools`, `smartmontools`
- Windows: PowerShell 5+
- Root/sudo for: temperature sensors, disk SMART, nethogs

---

## License

MIT
