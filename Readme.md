Here is the updated README.md for your GitHub repository. I have included the "House" analogy for your son, the specific steps for Google and OpenRouter, and the exact "Android Fixes" we used to stop the bot from crashing.
🤖 OpenClaw Mobile Station (UK Edition)
🏠 The Story: Building a House for an AI
Imagine your phone is a busy city. Usually, you only see the shops (Apps) that Google lets you visit. But we want to build our own Private Laboratory inside the city where our AI helper can live and work.
1. The Empty Plot: Termux
Before you build a house, you need a piece of land. Termux is like a magic "Empty Plot" inside your phone. It’s a special space where we can build whatever we want without the rest of the phone interfering.
2. The House Structure: Ubuntu
Now we have the land, but we need walls and a roof. Ubuntu is a full computer system (Linux) that we put inside Termux. It’s like putting a sturdy brick house on our empty plot.
3. The Furniture: OpenClaw
A house isn't useful if it's empty! OpenClaw is the furniture.
 * It’s the Desk where the AI writes its reminders.
 * It’s the Telephone (Telegram) it uses to talk to you.
 * It's the Brain (LLM) that tells the furniture how to move.
🛠 Step-by-Step Construction Guide
Phase 1: Preparing the Ground (Termux)
 * Download Termux (from F-Droid).
 * Open it and type these magic words to make the ground ready:
   pkg update && pkg upgrade

 * Install the "Building Kit" (proot-distro):
   pkg install proot-distro

Phase 2: Building & Entering the House (Ubuntu)
 * Build the Ubuntu house:
   proot-distro install ubuntu

 * Walk inside:
   proot-distro login ubuntu

Phase 3: Moving the Furniture In (OpenClaw)
Now that you are inside the Ubuntu house, run the installer:
curl -fsSL https://openclaw.ai/install.sh | bash

🚀 Phase 4: Connecting the Brains
1. The "Free Tier Hero": Google Gemini
We started here because it's free!
 * The Step: Go to Google AI Studio, click "Get API Key," and copy it.
 * The Setup: In Termux, type openclaw onboard. Select Google AI and paste your key.
2. The Professional Upgrade: OpenRouter
If Google gets tired (Error 429), we use OpenRouter. This lets the bot use many different brains (like Claude or GPT) using one wallet.
 * The Step: Get a key from openrouter.ai.
 * The Setup: ```bash
   openclaw models auth add --provider openrouter
   openclaw models set openrouter/openrouter/auto
   

🔧 Phase 5: Troubleshooting (The "Fix-It" List)
If the bot stops working, check these common fixes we discovered:
1. The "Bionic Bypass" (Crucial for Android)
Android phones have a special security rule (Bionic) that makes AI apps crash with an "Error 13" or "Networking Error." We fix this by giving the bot a "Fake Passport" so it doesn't try to look at the phone's hardware.
 * The Fix:
   # Inside Ubuntu, run this:
echo 'export OPENCLAW_DISABLE_BONJOUR=1' >> ~/.bashrc
source ~/.bashrc

2. The "429 Error" (Rate Limit)
If the bot says "Rate Limit Reached," it means you have talked to it too much today on the Free Tier.
 * The Fix: Wait 60 seconds. If it still doesn't work, wait until 8 AM UK time when Google resets your daily credits.
3. The "Deep Sleep" Fix (Keep it Alive)
Android likes to close apps that run in the background. To keep your bot awake:
 * The Fix: Swipe down your phone's notification bar. Find Termux and click "Acquire Wake Lock." This tells the phone, "Don't let this app sleep!"
📱 VitaNest Integration
VitaNest is our custom Android app. OpenClaw connects to it by writing data to a shared folder on the phone.
 * Reminders: Saved in ~/reminders.txt.
 * Grocery List: Saved in ~/grocery.txt.
 * Trading 212: Monitored via API and pushed to VitaNest.
🚀 Next Step
Now that your documentation is ready, you can create a new repository on GitHub and upload this file.
Would you like me to help you write the code for the "Saturday Grocery" script so you can add it to your new repository?
