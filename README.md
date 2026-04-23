# 🚀 Aether Code IDE - Installation & Setup Guide

Welcome to **Aether Code**, the AI-first desktop IDE for macOS! 
Follow these simple steps to get your environment up and running smoothly, and to connect your NVIDIA AI API.

---

## 🛠️ Step 1: Install the App
1. Locate the **`Aether-Code.dmg`** file in this folder.
2. Double-click the `.dmg` file to mount it.
3. Drag and drop the **Aether Code** icon into your **Applications** folder.

## 🔓 Step 2: Fix macOS Gatekeeper (Required)
Because Aether Code is downloaded outside the Mac App Store, macOS Gatekeeper might block it with a message saying *"App is damaged and can't be opened"*. This is a standard macOS security measure for unsigned apps.

To fix this immediately:
1. Open your **Terminal** app (Press `Cmd + Space`, type "Terminal", and hit Enter).
2. Copy and paste the following command, then press Enter:

   ```bash
   xattr -cr "/Applications/Aether Code.app"
   ```

## 🧠 Step 3: Get Your Free NVIDIA API Key
Aether Code is powered by NVIDIA's AI Catalog. To use the AI features (Chat, Code Generation, Vision, etc.), you need a free NVIDIA API key.

1. Go to **[build.nvidia.com](https://build.nvidia.com/)**.
2. Sign in or create a free NVIDIA account.
3. Navigate to any model (e.g., Llama 3.1) and click **"Get API Key"**.
4. Generate and copy your API Key (it usually starts with `nvapi-`).

## 🎉 Step 4: Launch & Configure!
1. Open your **Launchpad** or **Applications** folder and click on **Aether Code**.
2. When the app opens, click the **Settings** gear icon ⚙️ (usually in the bottom left).
3. Go to the **AI Providers** or **NVIDIA AI** tab.
4. Paste your API key into the NVIDIA API Key field and click **Save/Test Connection**.
5. You're ready to code with AI! 🚀 Choose the **Auto (Smart Switch)** model to let Aether Code automatically pick the best model for your tasks!

---

### 📦 What else is in this release package?
- **`/Assets`**: Contains high-quality Aether Code logos (useful for press, banners, or your own customization).
- **`README.md`**: Product overview, architecture, and features.
- **`Source-Code.tar.gz`**: The complete source code of this release.

*If you need further help, please refer to the main repository documentation!*
