# AI-Anomaly-Agent



# ShopFlow AI Anomaly Agent — My Upskilling Journey in Data Automation & AI

## 🧭 The Beginning: The Problem I Wanted to Solve
As a data enthusiast, I noticed a massive pain point in small businesses: managers receive endless Excel reports every week, but they don't have time to manually scan 52 rows of data to figure out which changes are "normal noise" and which are "emergencies." 
I wanted to build a system that does the boring, repetitive math so a manager can focus on *decisions*, not spreadsheets.

## 🛠️ The Build: My Step-by-Step Progression (From Stats to AI)
I decided to build this project from the ground up, writing every line of code myself. This project shows my evolution from a traditional data analyst to someone who can integrate modern AI tools.

**Phase 1: The Core Analytics Engine**
I started with pure Python and Pandas. I built a pipeline that:
- Ingests messy weekly CSV data and cleans it (handling date formats, empty columns, and inline text comments).
- Automatically calculates a **4-week rolling average baseline** and standard deviation.
- Uses a **Z-score threshold of 1.4** to mathematically detect which weeks are true outliers.

**Phase 2: The Business Intelligence Layer**
Instead of printing raw Z-scores (which mean nothing to a non-technical manager), I wrote a custom `if/else` logic engine that translates the math into plain-English sentences. 
- *Example:* "Revenue dropped 10.5%—check for supply chain issues."

**Phase 3: The AI Upgrade (Pushing Past Roadblocks)**
I decided to take this from a "good project" to a "next-level portfolio piece." I replaced the static `if/else` logic with a **free Google Gemini API** to generate richer, more human-like business explanations. 

*The Real-World Challenge:* During this upgrade, I hit a massive wall. Google kept returning `404 NOT FOUND` errors on multiple model names (`1.5-flash`, `2.0-flash-exp`, `gemini-pro`). Instead of giving up, I wrote a diagnostic script to pull Google's allowed model list directly from the backend, identified the dynamic `gemini-flash-latest` alias, and successfully connected the AI. **This experience taught me that real data work isn't about perfect tutorials—it's about stubbornly diagnosing and fixing API errors until the system works.**

## 📦 Project Architecture
- **Language:** Python 3 (Pandas, NumPy)
- **Environment:** Jupyter Notebook
- **Statistical Logic:** Z-Score analysis on 4-week rolling baselines
- **AI Layer:** Google Gemini (`gemini-flash-latest` via `google-genai` SDK)
- **Security:** Environment variables (`.env`) used to safely manage API credentials
- **Outputs:** `.txt` alert reports, CSV alert history logs, and AI-driven business summaries

## 🚀 Why This Project Makes Me Different From Other Students
Most student projects stop at the successful code block. 
- **I documented my failures.** My Jupyter notebook shows both the `if/else` foundation and the final AI upgrade, proving I didn't just copy a script—I built it.
- **I troubleshooted live APIs.** I didn't just plug in a library and walk away. When Google's deprecated models threw 404 errors, I analyzed the backend responses, fixed the integration, and made the system robust.
- **I separated concerns.** The statistical detection and the AI interpretation are separate layers, meaning you could easily swap out the AI model for a different provider without breaking the math.
- **I solved a genuine business problem.** Managers want *explanations*, not spreadsheets. This tool directly addresses that gap.

## 📂 How to Run This (No API Key Included)
1. Clone this repository.
2. Install the requirements: `pip install -r requirements.txt`
3. Open `anomaly_agent.ipynb` in Jupyter.
4. (Note: The API key is hidden in a local `.env` file for security. You will need to generate your own free Google Gemini API key to run the AI portion).
5. Run the notebook cells from top to bottom.

---

### 2. Your New, Completely Rewritten Interview Script

Here is a new script tailored to your journey. Read this out loud 2-3 times until it feels like your own words.

**Part 1: The Hook (30 seconds)**

> *"I built an automated Anomaly Detection Agent for business data. I started this project because I realized that business managers waste hours combing through spreadsheets, trying to figure out which weekly changes are normal noise and which require immediate action. My goal was to automate the math and deliver the signal, not the noise."*
