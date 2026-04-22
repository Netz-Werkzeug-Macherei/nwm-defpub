# Netz-Werkzeug.Macherei (#NWM)

## Datensouveränes Wissensmanagement mit hybrider KI-Architektur

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Status: v3.2](https://img.shields.io/badge/Version-v3.2-blue.svg)]()
[![Prior Art](https://img.shields.io/badge/Type-Defensive%20Publication-green.svg)]()
[![DOI|188](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.19699717-orange.svg)](https://zenodo.org/records/19699717)

> *"Das sind keine Chats, das sind Schätze!"*

---

## 🎯 Über das Projekt

Willkommen bei der **Netz-Werkzeug.Macherei (#NWM)**. Dieses Repository dokumentiert eine **Defensive Publication** für eine dezentrale, datensouveräne KI-Systemarchitektur, speziell konzipiert für:

- **Souveräne Einzelorganisationen:** KMUs, Vereine, NGOs, Gemeinden, Interessensgemeinschaften
- **Datenschutzbewusste Einzelanwender:** Heim-Server-Betreiber, Privacy-First-Anwender

**Ziel:** Sicherung des Standes der Technik (Prior Art) gemäß §3 PatG (DE) bzw. Art. 54 EPÜ – damit diese Architektur **frei nutzbar bleibt** und nicht von Dritten patentiert werden kann.

---

## 📋 Was ist eine Defensive Publication?

Eine **Defensive Publication** ist eine öffentliche Veröffentlichung einer technischen Lösung, um zu verhindern, dass Dritte diese später patentieren können. Der Zeitstempel der Veröffentlichung etabliert den "Stand der Technik", an dem niemand mehr vorbeikommt.

**Wichtig:** Die Lizenz (CC BY-NC-SA 4.0) schützt nicht vor Patenten. Es ist die Veröffentlichung selbst (mit überprüfbarem Zeitstempel), die schützt.

**Mehrfache Zeitstempel-Sicherung:**
- ✅ Eigene Domain: [netz-werkzeug-macherei.de](https://netz-werkzeug-macherei.de)
- ✅ Zenodo (CERN): DOI-basiert, wissenschaftlicher Goldstandard
- ✅ Wayback Machine: Unabhängiger Drittanbieter
- ✅ GitHub: Diese Repo mit Git-History

---

## 🌟 Kernmerkmale (Anspruchskette M1–M7)

Die beschriebene Architektur zeichnet sich durch die folgende Merkmalskombination aus:

- **M1:** Lokale Verarbeitungsebene (iKi) mit Open-Weight-Modell (≥8B Parameter)
- **M2:** Vier-stufige PII-Filter-Pipeline (NER, semantische Umformulierung, reversibles Mapping, Verifikation)
- **M3:** Deterministisches Human-in-the-Loop (HITL) Gate mit Trigger-Mechanismus, Diff-Visualisierung und Audit-Logging
- **M4:** RAG-Anbindung an selbstgehostete SSOT-Plattform mit RBAC
- **M5:** Multi-Provider-Routing mit ZDR-Policy
- **M6:** Optionale Föderationsschicht über VPN
- **M7:** Optionale Multimodal-Erweiterung (Text, Bild, Audio, Video)

---

## 🛠️ Tech Stack (Referenz-Implementierung)

Das System ist **technologie-agnostisch**. Folgende Komponenten dienen als Referenz:

| Komponente | Technologie (Beispiele) | Zweck |
| :--- | :--- | :--- |
| **Plattform (SSOT)** | Nextcloud, OwnCloud, Seafile | Dateien, Wiki, Kommunikation |
| **Lokale KI (iKi)** | Ollama, LM Studio, Msty Studio | Lokale LLM-Ausführung (8B–13B) |
| **Cloud Gateway (cKi)** | OpenRouter.ai, direkte APIs | Zugang zu größeren Modellen (70B+) |
| **Orchestrator** | Python (FastAPI), n8n, Node-RED | Routing & Workflows |
| **Vektor-DB (RAG)** | ChromaDB, Qdrant, LlamaIndex | Embedding-Speicher |
| **Agenten** | LangChain, AutoGen, CrewAI, OpenClaw | Workflow-Automation |
| **Client** | Obsidian, Browser | Lokale Notizen, UI |
| **VPN** | Tailscale, WireGuard | Sicherer Fernzugriff |
| **Verschlüsselung** | Cryptomator | Client-Side Encryption |

**Plattform-Unabhängigkeit:** Windows, Linux und macOS werden alle unterstützt.

---

## 📚 Dokumente

| Datei | Beschreibung | Datum |
| :--- | :--- | :--- |
| [v3.2 (aktuell)](./docs/1_Defensive-Publication_NWM_v3.2.pdf) | Aktuelle Version mit präzisierter Architektur | 22.04.2026 |
| [v3.0 (Erstveröffentlichung)](./docs/1_Defensive-Publication_NWM_v3.0.pdf) | Erste öffentliche Veröffentlichung | 15.04.2026 |
| [CHANGELOG](./CHANGELOG.md) | Versionshistorie | – |

---

## 🎓 Für wen ist das?

| Zielgruppe | Bisherige Lösungen | NWM-Ansatz |
| :--- | :--- | :--- |
| **KMU (<500 MA)** | Keine spezifischen integrierten Lösungen | **Hybride Orchestrierung mit lokaler Souveränität** |
| **Vereine/NGOs** | Generische Cloud-Tools | **Self-hosted mit Team-Funktionen** |
| **Einzelanwender** | PrivateGPT, Ollama (kein Team) | **Team-fähig + Sovereignty** |
| **Heim-Server-Betreiber** | Bastellösungen | **Strukturierte Architektur** |

---

## 🚀 Quick Start (für Implementierer)

> ⚠️ **Hinweis:** Dies ist eine Architektur-Dokumentation, **keine fertige Software**. Sie dient Implementierern als Leitfaden.

1. **Architektur verstehen:** Lies die [DefPub v3.2](./docs/1_Defensive-Publication_NWM_v3.2.pdf)
2. **Hardware prüfen:** GPU mit ≥16GB VRAM (z.B. RTX 4060 Ti 16GB)
3. **Sicherheit zuerst:** VPN-Tunnel einrichten, KEINE offenen Ports
4. **Plattform wählen:** Nextcloud (Self-Hosted oder Managed Hosting)
5. **iKi installieren:** Ollama mit Llama-3.1 oder Mistral
6. **Routing implementieren:** Sensibilitäts-basierte Logik (siehe DefPub Abschnitt 4.2.3)
7. **HITL aktivieren:** Niemals automatische Cloud-Übermittlung
8. **Guardrails konfigurieren:** ZDR-Policy, Regionale Compliance, Inhaltsfilter

---

## 🗺️ Roadmap

- [x] Konzeptphase & Architekturdefinition
- [x] Defensive Publication v3.0 (15.04.2026)
- [x] Defensive Publication v3.2 (22.04.2026)
- [x] Zenodo-Veröffentlichung mit DOI
- [x] Wayback Machine Snapshots
- [x] GitHub Repository (dieses Repo)
- [ ] Dokumentation der RAG-Pipeline (Code-Beispiele)
- [ ] Docker-Compose für Referenz-Setup
- [ ] Sicherheits-Audit-Leitfaden
- [ ] Community-Erweiterungen
- [ ] v3.3 (geplant: ca. Q3/2026)

---

## 🤝 Mitmachen

Beiträge sind willkommen! Wir freuen uns über:

- **Issues:** Fragen, Anregungen, Korrekturen
- **Pull Requests:** Verbesserungen der Dokumentation
- **Diskussionen:** Erfahrungsberichte, Use Cases, Best Practices

**Bitte beachten:**
- Keine proprietären Abhängigkeiten, die die Selbsthosting-Fähigkeit einschränken
- Fokus auf Datenschutz und Sicherheit
- Dokumentation aller Änderungen

---

## 📄 Lizenz

Die Dokumentation und das Konzept stehen unter der **CC BY-NC-SA 4.0 Lizenz**:

- ✅ **Namensnennung:** Sie müssen den Urheber nennen
- ❌ **Nicht kommerziell:** Keine kommerzielle Nutzung der Dokumentation
- 🔄 **Weitergabe unter gleichen Bedingungen:** Bearbeitungen unter gleicher Lizenz

**Hinweis:** Code-Skripte (sofern später hinzugefügt) können abweichende Lizenzen tragen (z.B. MIT), sofern explizit gekennzeichnet.

**WICHTIG:** Diese Lizenz gewährt **keine Patentrechte**. Die Defensive Publication schützt vor Patentierung durch Dritte, nicht vor bestehenden Patentrechten Dritter.

---

## 📞 Kontakt

- **Website:** [netz-werkzeug-macherei.de](https://netz-werkzeug-macherei.de)
- **Issues:** [GitHub Issues](https://github.com/Netz-Werkzeug-Macherei/nwm-defpub/issues)
- **Zenodo:** [DOI Link](https://zenodo.org/records/19699717) 

---

## ⚖️ Haftungsausschluss

Diese Veröffentlichung beschreibt ein **Architekturkonzept**. Die tatsächliche Sicherheit im Betrieb hängt von der korrekten Implementierung durch den Betreiber ab.

Alle genannten Produkte sind Warenzeichen ihrer jeweiligen Eigentümer. Die Nennung stellt keine Empfehlung dar.

Die rechtliche Zulässigkeit konkreter Implementierungen (DSGVO, EU AI Act, AGBs externer Dienste) ist im Einzelfall zu prüfen.

---

## 🦉 Schlusswort

> *"Wir glauben an ein Ökosystem, in dem Datensouveränität ein Grundrecht und kein Luxusgut ist."*

**Netz-Werkzeug.Macherei** – *Unabhängigkeit durch Technologie.*

 *"... mit dem Sinn für Verbindungen und Zusammenhänge."*
