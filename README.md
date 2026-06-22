#whoami

# Stephen Onserio
### AI-Augmented Product Engineer · Offensive Security · Civil Engineering


## Whoami


I build a parallel path as an AI-augmented product engineer and offensive security
practitioner through through shipped systems, documented
exploits, and real hardware.


## What I Build

### AquaSmart v5.1 — Intelligent Water Purification System

An IoT water purification system removing dissolved salts, heavy metals (Fe, Cd, Mn,
As, Cr), and pathogens from contaminated water. 7 stages. Gravity-fed. Offline-capable.

Hardware: Arduino Uno, L298N motor drivers, LM358 op-amp, TDS sensors, ZGA25RP
gearbox motor, relay-controlled UV-C, carbon rod electrodes, aluminium EC plates,
activated charcoal CDI pouches, bone char, mineral stones.

The analytical core is DPASV — Differential Pulse Anodic Stripping Voltammetry —
implemented on Arduino. The same electrochemical detection technique used in
professional analytical labs, rebuilt at $3 component cost. It sweeps voltage across
a graphene oxide working electrode and identifies heavy metals by their characteristic
reduction potentials: Fe at −0.5V, Cd at −0.6V, Mn at −0.7V, As at −0.8V, Cr at −0.9V,
each checked against WHO thresholds before water is cleared.

AI layer: A web dashboard (v26, single HTML file) hosts AQUA Agent — an LLM interface
powered by Groq API (LLaMA 3.3 70B) that interprets sensor readings, flags contamination
events, and delivers safety verdicts in plain language. The dashboard runs SHA-256 hash
chains on all audit logs (pAudit), a SCADA control interface with 3-attempt lockout and
30-minute session timeout, 4 role-based access levels, and a multilingual ticker in
English, Swahili, Kikuyu, and Kamba.


### NBO FloodMap — Flood Intelligence Platform

Real-time flood risk mapping for Nairobi. All 85 wards covered with GeoJSON boundaries.
Live rainfall data from Open-Meteo. Citizens report floods via the platform. AI validates
photo reports before they go live. County engineers see contamination risk patterns and
Flood Risk Index scores per ward in real time.

AI layer: "Saidika" — a bilingual AI chatbot (Groq LLaMA 3) answering flood and
drainage questions in English and Swahili. Photo validation uses Claude Haiku to reject
false or irrelevant reports before they pollute the map. SMS alerts via Africa's Talking.


### Ferret — NoSQL Injection Testing Tool

Python-based MongoDB injection testing framework. 5 modules: detect, bypass, extract,
blind, report. Full CLI interface. Built as a learning artifact during the ethical
hacking curriculum — now part of the public pentest portfolio.

→ github.com/onxerio/ferret

---

## AI Engineering

I use AI at every layer — as a code generation engine, a reasoning interface for
sensor data, a document validator, a conversational interface for end users, and an
audit tool. Current stack and areas of active study:

**Inference & APIs**: Anthropic Claude (Haiku, Sonnet), Groq (LLaMA 3.3 70B),
OpenAI-compatible endpoints. Prompt engineering, system prompt architecture,
multi-turn conversation design, structured JSON output via constrained prompting.

**Agentic frameworks**: LangChain (chains, memory, tool use), CrewAI (multi-agent
task delegation). Building toward autonomous agents that can reason over sensor
data and take action without human-in-the-loop for each step.

**AI red teaming**: OWASP Top 10 for LLMs. All 8 LLM security labs completed via
PortSwigger. Active study of prompt injection, jailbreaks, model inversion, data
poisoning, and indirect injection through tool outputs. I approach LLM security the
same way I approach web application security — find the trust boundary, break it,
document it.

**TinyML**: On-device inference on embedded hardware. Relevant to AquaSmart — the
goal is a model that can run contamination classification locally on Arduino or ESP32
without any cloud dependency.


## Offensive Security

Active home lab. Three machines: Kali Linux (attacker), Windows Server AD DC
(... domain: lab.local), Metasploitable2 (Linux target).

**Completed:**
- Windows enumeration, privilege escalation (WinPEAS)
- Active Directory: Kerberoasting, Pass-the-Hash, DCSync, Golden Ticket
- Network: EternalBlue (MS17-010)
- Linux privilege escalation (5/6 vectors complete)
- Web: XSS, SQLi (manual + SQLmap), CSRF, SSRF, XXE, JWT attacks, API security,
  LLM/AI security — all practiced via PortSwigger Web Security Academy labs

**In progress:**
- BloodHound AD attack path mapping
- Mimikatz credential extraction
- noPac (CVE-2021-42278/42287)
- Responder LLMNR/NBT-NS poisoning
- Linux kernel exploit (final privesc vector)
- Metasploit advanced, Burp Suite full workflow, Hashcat, Gobuster, Wireshark

All documented.

→ github.com/onxerio/pentest-portfolio

---

## Currently Learning

- AI red teaming — LLM attack taxonomy, OWASP LLM Top 10
- Agentic AI engineering — LangChain, CrewAI
- TinyML — on-device inference for embedded systems
- Active Directory advanced attack paths


## Contact

stephenonserio10827@gmail.com
GitHub: @onxerio