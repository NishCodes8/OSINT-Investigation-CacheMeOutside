# OSINT-Investigation-CacheMeOutside
Simulated threat-actor tracking and digital-footprint investigation using passive and active OSINT.
# Threat Intelligence Case Study: Tracking a Retired Threat Actor (Cache Me Outside)

**Executive Summary
A multi-phase Open-Source Intelligence (OSINT) investigation into a simulated target (`jiml33t`). This investigation demonstrates passive footprinting, advanced version-control metadata analysis, active OSINT interaction, and physical geolocation mapping.

---

## 🛠️ Tools & Methodologies Used
* **Passive OSINT:** Platform cross-referencing, digital footprint analysis.
* **Metadata & Git Analysis:** Exposed commit history parsing (`.patch` formatting).
* **Active OSINT:** Interactive communication with target infrastructure.
* **Geolocation:** Map analysis, local infrastructure cross-referencing.

---

## 🔍 Investigation Phases

## Phase 1: Initial Footprinting & Platform Pivoting

### Methodology & Concepts Learned
* **Platform Pivoting:** Tracked the target's handle across third-party platforms starting from an initial Komoot profile URL.
* **Profile Metadata:** Analyzed bio information and linked social accounts to uncover secondary developer handles.

### Key Findings
* **Target Display Name:** Jim Lee
* **Target GitHub Handle:** `jiml33t`

---

## Phase 2: Version Control Inspection & Active Engagement

### Methodology & Concepts Learned
* **Git Commit Metadata Leakage:** Learned that profile privacy settings on GitHub do not retroactively alter local commit metadata. Git hardcodes `user.email` into commits locally.
* **Patch Inspection (`.patch`):** Appended `.patch` to a commit URL to force GitHub to serve the raw Unix patch headers, revealing the author's local email configuration.
* **Active OSINT (Auto-Responders):** Sent an inquiry email to trigger automated "Out-of-Office" responses to extract secondary communication channels.

### Key Findings
* **Exposed Email:** `jimleepro1@gmail.com`
* **Exposed Phone Number:** [Phone number from auto-reply]

![Git Patch Email Proof](assets/active-osint-email.png)

---

## 🛡️ Key Defensive Takeaways (OpSec Failures)
1. **Metadata Exposure:** Version control commits can expose private email addresses if git configurations are not sanitized.
2. **Interactive Assets:** Unmonitored or default auto-responders create active intelligence vectors for attackers.
3. **Visual Indicators:** Photos containing identifiable regional landmarks or businesses can lead to precise geolocation.
