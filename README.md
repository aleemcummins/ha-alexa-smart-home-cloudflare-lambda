# Home Assistant + Alexa Smart Home Skill via AWS Lambda + Cloudflare Tunnel

?? **Important**

This guide uses placeholder domains such as:

https://ha.yourdomain.com

Replace them with your own Home Assistant external URL.

---

# Overview

This guide shows how to connect **Amazon Alexa** to **Home Assistant** using a **custom Alexa Smart Home Skill** backed by **AWS Lambda**, with Home Assistant exposed securely via a **Cloudflare Tunnel**.

This approach allows Alexa to control Home Assistant devices **without using Nabu Casa**.

---

# Architecture

Alexa  
? Alexa Smart Home Skill  
? AWS Lambda  
? Home Assistant (`https://ha.yourdomain.com`)  
? Devices (lights, switches, automations)

---

# Architecture Diagram

```mermaid
flowchart LR
  A[Alexa Voice or Alexa App] --> B[Alexa Smart Home Skill]
  B --> C[AWS Lambda]
  C --> D[Home Assistant https://ha.yourdomain.com]
  D --> E[Lights Switches Covers Automations]