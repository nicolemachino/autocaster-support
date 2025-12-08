# Autocaster – Public Support Repository

Welcome to the **public support and issue-tracking repository** for **Autocaster**.

Autocaster is an application designed to provide **automatic live directing** for **NewTek TriCaster** production systems.  
It observes microphone activity, selects the most relevant camera shot based on editorial rules, and communicates with the TriCaster using both **WebSocket** and **HTTP** APIs.  
The system includes a web-based UI for configuration, monitoring, and operational control.

⚠️ **Important:**  
This repository contains **no source code**.  
The actual implementation is private and proprietary.  
This space is only used to collect bug reports, feature requests, and general questions.

---

## 🔎 What Autocaster Does (High-Level Overview)

Autocaster acts as an automated vision mixer assistant, making real-time decisions based on studio activity:

### 🎥 **Automatic Shot Selection**
- Detects microphone activity from the TriCaster.  
- Chooses the most relevant camera and preset (close-ups, group shots, beauty, special shots).  
- Applies timing rules (focus, unfocus, jitter, delays for PTZ/fixed/semi-fixed shots).

### 🎛️ **TriCaster Integration**
- WebSocket: microphone levels, tally, states.  
- HTTP Shortcuts & Macros: camera presets, framebuffer updates, on-air macros, etc.  
- Datalink support.

### 📄 **DIGAS / XML Integration**
- Monitors an XML file for keywords.  
- Allows triggering actions, macros, scenarios, datalink pushes, or thumbnail retrieval.

### 🌐 **Web Interface**
- Dashboard: real-time monitoring (current shot, next shot, mic states, DIGAS activity, system status).  
- Configuration pages: shows, cameras, mics, presets, special shots, triggers, TriCaster settings, thresholds.  
- Log viewer & system settings.  
- Dashboard Lite: simplified full-screen display for control rooms or multiviewers.

---

## ❗ What This Repository Is For

Use this space to:

### 🐛 **Report bugs**
If something doesn't behave as expected, please open an Issue with:
- A clear description  
- The expected behavior  
- The observed behavior  
- Steps to reproduce  
- Screenshots or logs if available  

### 💡 **Request enhancements**
If you have a feature request or workflow improvement:
- Explain your use case  
- Describe the desired behavior  
- Add any relevant examples  

### ❓ **Ask questions**
General questions about behavior, workflow, configuration, or integration are welcome.

---

## 📌 Before Creating an Issue

Please check:

- Existing open issues  
- Closed issues (maybe your question already has an answer)  
- That your request does not include sensitive information such as IPs, credentials, or internal network details  

Remember, this repository is public.

---

## 📬 How to Submit an Issue

When creating an issue:

1. Choose the appropriate **Issue Template** (Bug / Feature / Question)  
2. Fill in the requested fields  
3. Provide as much context as possible  
4. Avoid sharing private configuration details  

We aim to keep issue tracking clean, structured, and easy to follow for both maintainers and users.

---

## 📣 About Autocaster

Autocaster is developed by **Nicolas ROLLAND EI** for **RTS**  
All rights reserved.  
This repository does not grant any rights to the source code or internal implementation.

