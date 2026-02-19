This is a professional and clear README.md structure tailored for your project. It’s designed to be a "Blueprint" so your son (or anyone else) can understand the clever storage trick you used.
You can copy and paste this directly into your GitHub:
# 🤖 OpenClaw Hybrid Assistant (UK Edition)

A mobile-first, high-reliability AI assistant running locally on Android via Termux/Ubuntu. This project features a **Hybrid Brain** setup, using cloud intelligence for speed and an offline "Prepper Brain" for internet-free failsafes.

## 🌟 Key Features
* **Dual-Brain Logic:** Uses OpenRouter (Cloud) as primary and DeepSeek-R1 (Local) as backup.
* **SD-Card Optimized:** All heavy AI models are offloaded to external storage to keep the 106GB internal phone memory free.
* **UK Contextualized:** Configured for UK-specific tasks like grocery price tracking (Tesco/Lidl) and VAT calculations.

---

## 🏗️ System Architecture

### 🏠 The Environment
* **OS:** Ubuntu (via Proot-Distro in Termux)
* **DNS:** Configured to `8.8.8.8` (Google) for stable house-to-street connectivity.
* **Engine:** Ollama (The AI Librarian).

### 💾 Storage Strategy (The SD-Card Trick)
To prevent the phone from running out of space, we use a **Symbolic Link** to "tunnel" data from the internal Ubuntu folder to the SD card.
* **SD Card ID:** `3238-6661`
* **Internal Link:** `~/.ollama/models`
* **Real Path:** `/storage/3238-6661/Android/data/com.termux/files/ollama_models`

---

## 🧠 The Offline Brain: DeepSeek-R1 (1.5B)
The local model is **DeepSeek-R1**, a 1.1GB "Reasoning Model."
* **Capabilities:** Chain-of-Thought thinking, logic puzzles, coding, and offline UK grocery planning.
* **Location:** Confirmed 100% on SD card (Internal storage impact: 0GB).

---

## 🛠️ Maintenance Commands

### 1. Start the AI Motor
If the bot isn't responding offline, ensure the Ollama service is running:
```bash
ollama serve &

2. Verify Storage Integrity
Check that the brain hasn't "leaked" into internal memory:
du -sh /storage/3238-6661/Android/data/com.termux/files/ollama_models
# Should return ~1.1G

3. Talk Directly to the Brain
For a direct terminal chat without using the OpenClaw gateway:
ollama run deepseek-r1:1.5b

📋 Project History & Today's Milestone (19-Feb-2026)
 * ✅ Fixed Ubuntu DNS resolution issues.
 * ✅ Successfully installed Ollama engine.
 * ✅ Mapped symbolic link to External SD Storage.
 * ✅ Successfully pulled 1.1GB DeepSeek model to SD Card.
 * ✅ Verified API response (HTTP 200 OK via GIN).
Next Step: Integration of the Saturday Grocery Script (Tesco/Sainsbury's API).

---

### 💡 Tip for GitHub:
When you save this file, if you name it `README.md` (all caps), GitHub will automatically turn it into a beautiful landing page with bold headings and clear code boxes.

**Would you like me to help you write the `groceries.py` script next, or should we set up the "Auto-Start" script so the bot wakes up automatically when the phone reboots?**

