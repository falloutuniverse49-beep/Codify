# Codify

<img width="1254" height="1254" alt="Пиксельный помощник у терминала" src="https://github.com/user-attachments/assets/a6531bcb-c0ba-48c2-bf5e-ac1338542486" />


[![Tauri](https://img.shields.io/badge/Tauri-2.0-blue.svg?style=flat-square&logo=tauri)](https://tauri.app/)
[![Rust](https://img.shields.io/badge/Rust-1.75+-orange.svg?style=flat-square&logo=rust)](https://www.rust-lang.org/)
[![React](https://img.shields.io/badge/React-18-blue.svg?style=flat-square&logo=react)](https://reactjs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

**Codify** is a Windows desktop GUI client designed to replace terminal-based workflows with AI tools (Claude Code, Codex CLI, etc.). Built with Tauri 2 (Rust + React), it operates fully autonomously.

### Features

The application includes the following capabilities:

*   **Universal API Client:** Support for any API or gateway (OpenAI-compatible, Anthropic). Multi-model support (one API key and Base URL — access to dozens of models).
*   **Flexible Permission System:** "Safe", "Standard", and "YOLO" modes. Custom rules (directory blacklists, script execution blocking). Token limits with automatic task pause.
*   **Context Management:** Workspaces for setting the base directory. Effort levels with *Ultracode* mode (dynamic workflow orchestration with visual effects). Clear and Compact history actions.
*   **Workflows:** A pinned "Workflows" button in the session sidebar. It provides access to dynamic workflow management (listing running and completed workflows, progress tracking, and cancellation). **Available only when a Claude model is selected**; the button is disabled and greyed out for other models.
*   **Media Rendering:** Displays generated images and videos directly in the chat feed. "Open file" button (highlights the file in Windows Explorer).
*   **Attachments:** File attachment via click (paperclip) or Drag-and-Drop.
*   **Plugin System:** Custom profile installation via `.zip` (Drag-and-Drop), with hot-reload support.
*   **Design:** Premium dark-beige Claude-inspired theme. Custom animated 8-bit pixel spider mascot.

### Installation

Distributed as a standalone installer, `CodifySetup.exe`.
*   No Node.js, Python, or Rust required on the host machine.
*   No admin rights required (installs to `%LOCALAPPDATA%`).
*   Works offline (bundles the WebView2 installer).

### Tech Stack
*   **Backend:** Rust, Tauri 2, Tokio, Reqwest, Keyring (Windows Credential Manager).
*   **Frontend:** React 18, TypeScript, Vite, Tailwind CSS, Framer Motion, Zustand.

### Build
```bash
npm install
npm run tauri dev
