---
name: user-guide
description: "HanaAgent user reference: features, setup, agents, memory, Bridge, skills, plugins, security. Triggers: how to use, help, tutorial, feature reference."
---

# HanaAgent User Guide

HanaAgent is a local-first AI assistant with memory, file system access, multi-agent support, and cross-platform Bridge.

## Core Concepts
- **Agent**: An independent assistant with its own persona (ishiki), thinking framework (Yuan), memory, and conversation history. Create multiple agents in Settings → Assistants.
- **Yuan**: Thinking framework. Four options: Hanako (balanced), Butter (emotional), Ming (rational), Kong (raw model).
- **Ishiki**: Agent persona — free-text identity definition in Settings → Assistants → Ishiki.
- **Memory**: Multi-tier natural-decay system: conversation → rolling summary → daily compilation → weekly compilation → long-term → fact base → pinned. Manage in Settings → Assistants.
- **Experience**: Learned workflows and error-correction patterns from past work. Separate from factual memory. Use `/xing` to extract reusable workflows.

## Interface
- **Input**: Send (Enter), newline (Shift+Enter), attach files (drag or button), stop generation, steer (interrupt mid-response).
- **Thinking depth**: Off/Low/Medium/High/Very-High toggle. Higher = deeper reasoning, slower response.
- **Access mode**: Operate (allow all tools) / Ask (prompt before writes) / Read-only (no file writes or commands).
- **Slash commands**: `/compact` (compress context), `/diary` (archive session), `/xing` (extract workflow), `/stop`, `/new`, `/reset`.
- **Context ring**: Shows token usage. Click to compact when near limit.
- **Desk (right panel)**: File browser, notepad editor (Markdown with preview), skill shortcuts. Drag files into chat.
- **Preview panel**: Renders code, Markdown, CSV, HTML, charts, LaTeX. Tab-switch, fullscreen, copy, download, cite to input.

## Bridge (Cross-Platform)
- Connect to Telegram, Feishu, QQ, WeChat. Settings → Social Platforms.
- **Owner**: Must set your platform user ID as Owner for full permissions. Without Owner, messages are treated as guest.
- **WeChat exception**: iLink private channel auto-identifies as Owner.
- **Remote session**: `/rc` in Bridge DM to take over a desktop session. `/exitrc` to release.
- **Files**: Unified SessionFile system; platform-specific delivery.

## Automation
- **Cron tasks**: Describe schedule in chat. View/manage in Automation panel.
- **Heartbeat**: Periodic workspace inspection. Enable in Settings → Desk. Interval: 1–120 min.

## Skills & Plugins
- **Skills**: Markdown knowledge files auto-loaded on relevant triggers. Install via drag-drop `.skill`/`.zip`/folder. Sources: built-in, user-installed, self-learned, external. Enable per-agent in Settings → Skills → Agent toggle.
- **Plugins**: Add tools, commands, pages, widgets. Restricted or Full-access. Hot-reload on install/enable.
- **MCP connectors**: Settings → Connectors. Local (command-launched) or remote (URL + OAuth/Bearer). Per-agent tool control.

## Security
- **Sandbox**: Limits file access scope. Sensitive dirs protected by default.
- **File backup**: Auto-saves originals before modification.
- **Access mode + sandbox**: Together define the security boundary.
- **Computer control** (experimental): Settings → Computer Use. App-by-app approval.

## Personalization
- **Themes**: Warm Paper, Midnight, High Contrast, Grass Aroma, Contemplation.
- **Font**: Serif toggle, Markdown margin width.
- **Language**: Simplified/Traditional Chinese, Japanese, Korean, English.

## Tips
- "Remember: [fact]" → pins to permanent memory.
- "Create a skill for [purpose]" → HanaAgent writes and installs SKILL.md.
- Describe automation → HanaAgent writes script and creates cron task.
- Multi-Agent: create specialized agents, open a channel, let them discuss.

## Troubleshooting
- **Agent doesn't remember**: Check memory toggle in Settings → Assistants.
- **Bridge replies short**: Owner not set correctly.
- **Skill installed but unused**: Enable for specific agent in Settings → Skills.
- **Plugin not working**: Check loaded status; may need full-access.
- **Thinking depth no effect**: Model may not support extended thinking.