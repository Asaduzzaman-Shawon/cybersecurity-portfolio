# 🐧 Month 01 — Linux Fundamentals, Networking & Python

<p>
  <img src="https://img.shields.io/badge/Phase-Foundation%20Builder-00c8f0" alt="phase" />
  <img src="https://img.shields.io/badge/Status-In%20Progress-ffd84d" alt="status" />
</p>

**Roadmap Phase:** Foundation Builder — Month 1 of 12

This month covers the absolute basics I need before touching any real hacking tool: comfort with the Linux command line, core networking concepts, and enough Python to automate small tasks. It ends with a hands-on project — a custom port scanner.

---

## 🐧 Part 1: Linux Fundamentals

**What I practiced:**
- *Navigation command*
- *File Operation*
- *Grep Text search*
- *Find File*
- *And I have complete OverTheWire Bandit Level 1 to 7*

**Key commands I got comfortable with:**
```bash
# example — replace with what you actually practiced
ls -la
pwd
cd 
du
find
mkdir
cp
mv
grep 
```

**Notes:**
*OverTheWire bandit level 1 to 6  was very easier for me, im using kali linux from today and i practice 5 to 6 hours, now im enjoying that*

**ScreenShots:**

<img width="325" height="215" alt="Capture" src="https://github.com/user-attachments/assets/17d17210-5abb-4363-a6a0-8187a72ba3f7" />



---

## 🌐 Part 2: Networking Basics

**Topics covered:**
- *(e.g., TCP/IP model, ports & protocols, DNS, subnetting basics)*

**Notes:**
*(2-4 lines summarizing what you understood — this matters later for Nmap in Month 2)*

![networking notes screenshot](./screenshots/02-networking.png)

---

## 🐍 Part 3: Python Fundamentals

**What I practiced:**
- *(e.g., variables, loops, functions, working with sockets/libraries)*

**Small exercise example:**
```python
# a short snippet from something you practiced
for i in range(1, 6):
    print(f"Practicing loop {i}")
```

**Notes:**
*(what felt natural, what needs more practice)*

---

## 🔧 Part 4: Final Project — Port Scanner

**Objective:** Build a basic TCP port scanner in Python to combine everything learned this month — sockets, loops, and basic networking concepts.

**Code:** [`scanner.py`](./scanner.py)

```python
import socket

def scan_port(target, port):
    sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    sock.settimeout(1)
    result = sock.connect_ex((target, port))
    if result == 0:
        print(f"Port {port}: OPEN")
    sock.close()

# usage example
target = "127.0.0.1"
for port in range(1, 1025):
    scan_port(target, port)
```

**How it works:** *(2-3 lines explaining the logic in your own words)*

**Result:**
```
Port 22: OPEN
Port 80: OPEN
```

![scanner output screenshot](./screenshots/03-scanner-output.png)

---

## 🧠 Overall Takeaway — Month 01

*3-4 lines: what you can actually do now that you couldn't a month ago. Be specific and honest — this is what an interviewer will probe on.*

> Example: I can now navigate Linux confidently, understand how data moves across a network at a basic level, and write simple Python scripts that interact with sockets — which directly builds into using tools like Nmap next month.

---

<p align="center"><a href="../README.md">← Back to Main Portfolio</a></p>

