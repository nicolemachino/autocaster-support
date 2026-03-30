# Autocaster Public Support

This repository is the public support, documentation, and issue-tracking space for **Autocaster**.

Autocaster is a live production assistant for **NewTek TriCaster** environments. It monitors microphone activity, applies editorial rules, and automatically selects the most relevant camera shot in real time.

This repository contains **no source code**.  
The implementation is private and proprietary.

## What This Repository Is For

Use this repository to:

- report bugs
- request features or workflow improvements
- ask support questions
- find public operational documentation
- follow public-facing product and support updates

## What Autocaster Does

Autocaster helps automate live directing workflows around TriCaster-based productions.

Main capabilities:

- monitors up to **8 microphones**
- works with **2 to 16 cameras**, depending on TriCaster configuration
- supports **PTZ**, **fixed**, and **semi-fixed** shot logic
- manages **close-ups**, **group shots**, **beauty shots**, and up to **4 special scenarios**
- integrates with TriCaster through **WebSocket** and **HTTP** APIs
- exposes a simple **Trigger In HTTP API** for external automation
- supports **DIGAS / XML-based** triggers and actions
- provides a web UI for configuration, monitoring, user management, and logs
- provides a simplified fullscreen **Dashboard Lite** view on `/dashboard`
- can generate a dashboard image for display in a **TriCaster buffer**

## High-Level Functional Overview

### Automatic shot selection

Autocaster observes microphone activity and decides which shot should be on air based on:

- microphone state
- camera assignment
- weights
- focus / unfocus / jitter timings
- PTZ / fixed / semi-fixed timing rules
- group shot availability
- beauty shot fallback
- special scenario triggers
- live dynamism level

### TriCaster integration

Autocaster communicates with TriCaster using:

- WebSocket for audio / tally state
- HTTP for macros, shortcuts, framebuffer operations, and DataLink

### Trigger In API

Autocaster can receive simple external commands through HTTP triggers.

Publicly documented trigger families include:

- `START`
- `STOP`
- `PAUSE`
- `RESUME`
- `FREEZE`
- `DYNAMISM`
- `DIGAS_ENABLE`
- `SHOW_LOAD`
- external event triggers for scenario workflows

### DIGAS / XML integration

Autocaster can monitor DIGAS-compatible XML sources and react to changes through configurable mappings such as:

- Autocam actions
- external events
- TriCaster macros
- DataLink updates
- dashboard information slots
- show loading
- thumbnail retrieval

### Web interface

The web UI is used for:

- live dashboard and control
- show creation and editing
- TriCaster settings
- DIGAS settings
- Trigger In settings
- user management
- log access and diagnostics

## Main Concepts

### Microphones

Each microphone can be associated with:

- a camera
- a close-up preset or macro
- a shot type
- editorial weight
- presence / listening timing
- focus / unfocus / jitter timings

### Shot types

Autocaster supports:

- `PTZ`
- `FIXE`
- `SEMI-FIXE`

These modes affect shot timing and switching behavior.

### Group shots

Autocaster supports logical group shots such as:

- `MIC1 + MIC2`
- `MIC1 + MIC2 + MIC3`

depending on the active show setup and shared camera logic.

### Beauty shots

Beauty shots act as fallback or breathing shots when editorial rules allow it.

### Special scenarios

Autocaster supports **4 special slots** that can be entered and exited through event-driven scenarios.

### Dynamism

Autocaster includes a live **dynamism** control that affects timing and editorial rhythm.

## User Roles

The UI supports at least two operational roles:

- `admin`: full configuration and administration access
- `operator`: operational access for live use

## Dashboard And Diagnostics

Autocaster includes:

- a main dashboard with live system status
- a fullscreen **Dashboard Lite** page at `/dashboard`
- current / next shot visibility
- DIGAS status visibility
- recent diagnostics and error visibility
- downloadable logs

## Logs

Autocaster keeps runtime logs intended to help troubleshooting and support.

Depending on configuration, logs can help diagnose:

- startup problems
- TriCaster connectivity issues
- missing macros
- DIGAS parsing or trigger issues
- dashboard capture / buffer issues
- Trigger In activity

## Before Opening An Issue

Please check:

- existing open issues
- closed issues
- relevant wiki / documentation pages

Because this repository is public, do **not** post:

- credentials
- internal IP addresses if they are sensitive
- customer-specific confidential information
- private network topology
- proprietary project files

## Recommended Information For Bug Reports

When possible, include:

- a short summary
- expected behavior
- actual behavior
- steps to reproduce
- whether the issue is constant or intermittent
- screenshots if relevant
- logs if available
- your Autocaster version
- TriCaster model/version if relevant
- whether the issue involves DIGAS, Trigger In, dashboard buffer, or show loading

## Recommended Information For Support Questions

When asking for help, include:

- what you are trying to achieve
- your current setup at a high level
- what already works
- what is blocked
- any relevant error messages

## Documentation

Recommended public documentation set:

- Getting Started
- Concepts
- Web Interface
- Trigger In API
- DIGAS Integration
- Dashboard and Diagnostics
- Deployment and Updates
- Troubleshooting
- FAQ
- Changelog

## About

Autocaster is developed by **Nicolas Rolland EI / MREV** for **RTS**.

This repository does not grant access to source code or implementation rights.  
All rights remain reserved.
