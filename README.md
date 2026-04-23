# Aether Code

Aether Code is an AI-first desktop IDE for macOS.

This repository README is written for GitHub visitors who want to understand **product logic and user flows**, not internal source details.

## What Aether Code Is

Aether Code keeps full IDE scope in one app:

- Welcome
- Explorer
- Editor
- AI Chat
- Model Registry
- AI Providers
- Terminal
- Remote (SSH)
- Migration (import from Cursor/Antigravity/VS Code)
- Extensions

## Core User Flow

1. App launch behavior
- If no workspace is open, the Welcome page appears.
- If a workspace is open, the workspace loads directly.

2. Welcome entry actions
- Open Folder
- New AI Workspace
- Clone Repository
- Recent Workspaces

3. Daily coding loop
- Open files from Explorer.
- Edit in Monaco editor.
- Use AI Chat for code generation and apply changes.
- Use Source Control for Git operations.
- Run commands in Terminal.

## Product Principles

- Do not remove major IDE surfaces.
- Broken surfaces are repaired, not hidden.
- Actions are functional, not decorative.
- Partial capabilities are labeled honestly.

## Extensions Logic (Important)

Extensions in Aether Code use an honest support model:

- `Full`: complete in-app support.
- `Partial`: integrated through built-in Aether surfaces.
- `Metadata`: install state is tracked, but full VS Code extension-host APIs are not yet available.

This avoids fake “installed = fully working” behavior.

## Remote SSH Logic

Remote SSH is a real surface in the product:

- Host list
- Add/Edit/Delete host
- Test connection with clear results
- Connect/Disconnect workflow

If deep remote extension runtime is not available, that is explicitly shown.

## Installation & Setup

1. Download the latest `.dmg` release from the repository.
2. Open the `.dmg` file and drag **Aether Code** to your **Applications** folder.
3. **Important macOS Gatekeeper Fix:** Because the app might be flagged by macOS as downloaded from the internet, you may see an "app is damaged and can't be opened" error. To fix this, open your Terminal and run the following command to clear the quarantine attributes:

```bash
xattr -cr "/Applications/Aether Code.app"
```

4. You can now open **Aether Code** from your Launchpad or Applications folder.

### 🧠 NVIDIA API Setup (Required for AI Features)
Aether Code uses NVIDIA's AI Catalog to power its features.
1. Go to [build.nvidia.com](https://build.nvidia.com/) and create a free account.
2. Generate an API Key (it starts with `nvapi-`).
3. Open **Aether Code**, go to **Settings ⚙️ > AI Providers**, and paste your API Key.
4. You are ready to go! Choose **Auto (Smart Switch)** in the chat to let the IDE pick the best model for you.

*Note for developers:* If you are building from source, the built DMG will be located at `src-tauri/target/release/bundle/dmg/`.

## Documentation For GitHub Visitors

Start here:

- [Product Guide Index](./docs/product-guide/README.md)

Main guide set:

- [Product Direction](./docs/product-guide/product-direction.md)
- [User Journeys](./docs/product-guide/user-journeys.md)
- [Feature Scope Matrix](./docs/product-guide/feature-scope-matrix.md)
- [Extensions Runtime Policy](./docs/product-guide/extensions-runtime-policy.md)
- [Remote SSH Workflow](./docs/product-guide/remote-ssh-workflow.md)

---

If you are visiting this repository to evaluate Aether Code quickly, read the folder `docs/product-guide/` first.
