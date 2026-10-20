# Voice Memo Ingestion: Stream-of-Consciousness Parsing Protocol

> **An open-source AI engineering protocol from [We Build for Good](https://webuildforgood.com)**  
> *Turn spoken founder brain-dumps into clean, prioritized execution.*

---

## Overview

`voice-memo-ingestion` is an operational protocol for AI assistants (Claude Code, Cursor, Antigravity, OpenAI Codex).

It gives AI assistants a consistent way to handle input from founders and engineers who dictate thoughts via Wispr Flow, speech-to-text, or audio voice notes. It cleanly separates exploratory brainstorms from immediate code tickets, preventing conversational chaos.

---

## The Four Buckets

* **Mindset & Context**: Emotional tone and high-level posture.
* **Brainstorming**: Creative ideas captured for later, never turned into immediate tickets.
* **Immediate Tickets**: Unambiguous tasks dispatched into code right away.
* **Rulings**: Final decisions codified into project memory.

---

## Installation

### For Claude Code
```bash
git clone https://github.com/We-Build-For-Good/skill-voice-memo-ingestion.git ~/.claude/skills/voice-memo-ingestion
```

### For Cursor
```bash
mkdir -p .cursor/skills
git clone https://github.com/We-Build-For-Good/skill-voice-memo-ingestion.git .cursor/skills/voice-memo-ingestion
```

### For Antigravity / Open Agent Skills
```bash
mkdir -p .agents/skills
git clone https://github.com/We-Build-For-Good/skill-voice-memo-ingestion.git .agents/skills/voice-memo-ingestion
```

---

## License

MIT License. Developed and maintained by [We Build for Good](https://webuildforgood.com).
