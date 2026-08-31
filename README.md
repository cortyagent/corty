# 🖥️ Corty: Remote Control for Your AI Coding CLIs

Welcome to the official public repository for **Corty**!
*Note: This repository does not contain the application source code. It serves as a centralized hub for our users to discover the app, report issues, and request new features.*

## 📖 About Corty

**Corty** is a free, self-hosted, cross-platform mobile app for developers who run AI coding agents — **Claude Code**, **Codex**, and **Antigravity** — in `tmux` on their own machine. Corty remote-controls those sessions from your phone: read the transcript, approve a risky command, answer a question, review the diff, all from wherever you are.

### ✨ Key Features

* **Approvals where they happen**: Allow once, always allow, or deny — inline in the transcript, or as one queue across every host. Risky commands are flagged before you tap.
* **Real questions, real answers**: Structured questions from the agent arrive as radios and checkboxes, answered as data. Arrow-key CLI menus still work — parsed and rendered as a tappable list.
* **Diffs you can actually read**: Word-level highlighting inside the changed line, indentation shown as dots, long hunks collapsed until you ask.
* **Reconnect-safe by design**: Output is buffered on the host and replayed from your last offset when you come back — a dropped subway connection doesn't lose your session. A wrong pairing token stops retrying instead of hammering forever.
* **A real terminal underneath**: Every session has a raw `tmux` pane one tap away — a true terminal emulator with a control-key row, not a text dump.
* **Broad CLI support**: Native protocol support for Claude Code and Antigravity, with Codex support built against its documented protocol. Anything else falls back to a PTY bridge with heuristic menu and approval detection.

### 🔒 Security-First Architecture

Your security is our top priority.

* **No Corty account, ever**: Corty has no backend of its own — no account system, no relay we control, no telemetry. Your phone talks straight to the host you configure.
* **Self-hosted, your infrastructure**: Sessions travel from your phone to your own machine over an authenticated WebSocket (direct, over Tailscale, or over your own self-hosted Netbird network) or your own SSH connection. Nothing is routed through us.
* **Hardware-backed local storage**: Host addresses, pairing tokens, and SSH keys are stored in your phone's secure storage. Session transcripts stay on-device by default, and can be turned off entirely.
* **Face ID / biometric gate**: Optionally require Face ID or fingerprint to open the app or to approve/deny an action.

---

## 🤝 Feedback, Bug Reports & Feature Requests

We want to build the best remote-control experience for AI coding agents. If you run into an issue or have an idea to make Corty better, we want to hear it!

1. **Bug Reports**: Found a glitch or something isn't working right? Please [open a Bug Report](https://github.com/cortyagent/corty/issues/new?template=bug_report.md).
2. **Feature Requests**: Have an idea that would make Corty even better? Please [submit a Feature Request](https://github.com/cortyagent/corty/issues/new?template=feature_request.md).
3. **General Questions**: Feel free to open an issue or reach out to our support.

*Before opening a new issue, please search the [existing issues](https://github.com/cortyagent/corty/issues) to see if it has already been reported.*

A good bug report answers five things: what you did and what happened instead; app version/platform (plus `corty-agent` version if you use the daemon); which CLI and whether the session was native or PTY fallback; connection mode (agent, SSH, Tailscale, or Netbird) and network (LAN, VPN, or tunnel); and any daemon log lines around the failure. Never paste your pairing token, SSH keys, or a transcript with secrets in it — redact first.

**Security issues**: please don't open a public issue. Use the repo's [security advisory form](https://github.com/cortyagent/corty/security/advisories/new) instead.

---

## 📩 Support & Contact

If you need private support or have business inquiries, you can reach out to us at:
📧 **Email**: richardpham201dev@gmail.com

---

### Links
- [Website](https://cortyagent.com/)
- [User guide](https://cortyagent.com/guide)
- [Help & bug reports](https://cortyagent.com/help)
- [Privacy Policy](https://cortyagent.com/privacy)
- [Terms of Service](https://cortyagent.com/terms)

---

*Claude Code, Codex, and Antigravity are products of their respective owners. Corty is an independent client and is not affiliated with or endorsed by them.*
