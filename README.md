# PhishGuard AI

> **Real-time phishing detection engine and mock Gmail extension prototype built for rapid email security analysis.**
> *Winner of the TedX Presentation Award at the April 2026 Cohort Hackathon.*

---

## Overview

**PhishGuard AI** is a lightweight, real-time threat detection system designed to inspect suspicious links inside email clients before users fall victim to credential harvesting or phishing scams. 

The prototype simulates an active Chrome Extension integrated into a mock Gmail interface. It performs dual-layer threat verification: an instant client-side heuristic inspection combined with an asynchronous AI classification engine.

---

## Key Features

* ** Dual-Layer Threat Detection:**
  * **Layer 1 (Client-Side Heuristics):** Analyzes domain structures locally for typosquatting, suspicious TLDs (`.tk`, `.xyz`), raw IP hostnames, excessive subdomains/hyphens, and urgent call-to-action phrasing.
  * **Layer 2 (AI Classifier):** Queries an LLM reasoning engine to generate a high-confidence threat verdict, risk category, and human-readable explanation.
* ** Real-Time UI Interception:** Replaces standard link clicks with a step-by-step loading analysis overlay and a comprehensive risk verdict popup.
* **Unified Risk Scoring:** Synchronizes individual link scan results with overall inbox risk badges (0–100%) in real time.
* ** Offline Fallback Mode:** Gracefully defaults to client-side heuristic evaluation if network latency or API limits occur.

---

## 🛠️ Architecture & Tech Stack

* **Front-End / UI:** Native HTML5, CSS3 (Google Sans styling, CSS Keyframes), Vanilla JavaScript (ES6+).
* **AI Integration:** Anthropic Claude API (`claude-3-5-sonnet` / `claude-sonnet-4`).
* **Algorithmic Logic:** Levenshtein Distance for typosquatting detection, regex-based TLD parsing, and deterministic baseline scoring.

---

## 🚀 Quick Start & Usage

Because the prototype is self-contained within a single executable HTML file, no complex server build step is required!

### Option 1: Direct Local Execution
1. Clone this repository:
   ```bash
   git clone [https://github.com/AaryanBadyal/phishguard-prototype.git](https://github.com/AaryanBadyal/phishguard-prototype.git)
