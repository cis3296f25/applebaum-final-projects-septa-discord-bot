<div align="center">

# SEPTA Discord Bot

[![Jira](https://img.shields.io/badge/Jira-KAN%20Board-blue)](https://tul32674.atlassian.net/jira/software/projects/KAN/boards/1)
[![Deploy Docs](https://github.com/ApplebaumIan/tu-cis-4398-docs-template/actions/workflows/deploy.yml/badge.svg)](https://github.com/ApplebaumIan/tu-cis-4398-docs-template/actions/workflows/deploy.yml)
[![Documentation Website Link](https://img.shields.io/badge/-Documentation%20Website-brightgreen)](https://cis3296f25.github.io/applebaum-final-projects-septa-discord-bot/)

</div>


## Keywords
Discord bot, Python, AsyncIO, SEPTA API, Real-time transit data


## Project Abstract
This project delivers a Discord bot that provides real-time SEPTA Regional Rail information to commuters. The bot integrates with SEPTA’s public APIs to display live train statuses, delays, station arrivals, outage alerts, and next-train predictions. Users can also subscribe to specific train lines and automatically receive notifications about delays or service interruptions. The goal is to create a simple, accessible, and community-friendly tool for anyone who uses SEPTA transit.


## High Level Requirement
The SEPTA Discord Bot must:

- Allow users to request real-time information using slash commands.
- Provide regional rail line status, station arrivals, and next train times.
- Handle user subscriptions and send automated delay/outage alerts.
- Normalize and validate station names for user-friendly interaction.
- Operate asynchronously to support multiple users simultaneously.
- Run reliably on Discord 24/7 with minimal manual intervention.


## Conceptual Design
- **Platform:** Discord  
- **Language:** Python  
- **Framework:** discord.py (with app_commands for slash commands)  
- **Architecture:**  
  - API Integration Layer (fetches SEPTA data via aiohttp)  
  - Command Handlers (slash commands such as `/next_train`, `/check_line_status`)  
  - Subscription System (stores user preferences and triggers alerts)  
  - Background Task Cog (periodically checks for outages or delays)  

The bot runs on an asynchronous event loop, enabling fast API calls and real-time interactions with multiple users.


## Background
SEPTA provides public real-time transit data through its APIs, but they are not always easy for riders—especially students—to navigate quickly. Existing tools like TrainView and NextToArrive work, but require manual refreshing and provide inconsistent formatting.

Discord, widely used by student groups and communities, provides an ideal platform to centralize SEPTA information in a simple interface. Similar transport bots exist for NYC MTA and other transit systems, but no modern Discord tool exists for SEPTA.

This project aims to create a reliable, convenient, and user-friendly alternative tailored to SEPTA commuters.


## Required Resources
**Software:**
- Python 3.10+
- discord.py library
- aiohttp for API calls
- SEPTA public API (no key required)
- GitHub Actions (for documentation deployment)

**Knowledge Requirements:**
- Asynchronous programming (async/await)
- REST API consumption
- JSON parsing
- Python classes and cogs (Discord bot architecture)

**Hardware:**
- None beyond a standard development environment.


## Collaborators
- Justin Pham  
- Jerry Lin  
- Christine Kapp  
- Chris Breeden  
- Fares Hagos  
