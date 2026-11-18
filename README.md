# Shut Up Hermes — Custom Discord Commands

![Custom Embeds](embeds_thumbnail.png)

> **Only the customized commands for Shut-Up-Hermes:** `/voice`, `/vc`, `/model`  
> Full manifest lives in [`Hermes-Slash-Command-Manifest`](https://github.com/Chimthuwu/Hermes-Slash-Command-Manifest-).

---

## 🎯 What This Is

A minimal, focused repository containing **only the Discord slash commands that Shut-Up-Hermes customizes**:

| Command | Purpose | Customized? |
|---------|---------|-------------|
| `/voice` | Toggle voice reply mode (join, channel, leave, on, tts, off, status) | ✅ Yes — custom embed + choices |
| `/vc` | Alias for `/voice` | ✅ Yes — same custom embed |
| `/model` | Show or change the model | ✅ Yes — custom model selection embed |

All other 28 native commands live in the [main manifest repo](https://github.com/Chimthuwu/Hermes-Slash-Command-Manifest-).

---

## 📦 Files

| File | Purpose |
|------|---------|
| `discord_commands.json` | **The manifest** — 3 commands with stable descriptions, options, choices, templates |
| `README.md` | This file |

---

## 🛡️ Why Separate?

Shut-Up-Hermes has **custom embeds and behavior** for these specific commands:
- `/voice` and `/vc` use a custom voice mode selection embed
- `/model` uses a custom model selection embed
- These customizations are Shut-Up-Hermes-specific

Keeping them separate means:
1. **Clear ownership** — you know exactly which commands have custom UX
2. **Independent versioning** — customize voice/model UI without touching core commands
3. **Easy sync** — pull main manifest for core, override just these 3

---

## 🔄 Workflow

### Update a Custom Command
1. Edit `discord_commands.json` — modify the command definition
2. Commit and push
3. Deploy to Shut-Up-Hermes (picks up on restart)

### Sync Core Commands
```bash
# From main manifest repo
git pull https://github.com/Chimthuwu/Hermes-Slash-Command-Manifest-.git
# Core commands updated, your 3 custom ones untouched
```

---

## 📋 The 3 Commands

### `/voice` — Toggle Voice Reply Mode
**Options:** `join`, `channel`, `leave`, `on`, `tts`, `off`, `status`  
**Custom:** Voice mode selection embed with rich formatting

### `/vc` — Voice Alias
**Same as `/voice`** — short alias with identical custom embed

### `/model` — Show or Change Model
**Options:** `name` (optional — leave empty to see current)  
**Custom:** Model selection embed with provider groupings

---

## 🔗 Related Repos

- **This repo:** `Shut-Up-Hermes` — only customized commands (3)
- **Main manifest:** [`Hermes-Slash-Command-Manifest`](https://github.com/Chimthuwu/Hermes-Slash-Command-Manifest-) — all 31 native commands

---

**Bottom line:** This is the override layer. Three commands, custom embeds, version-controlled. 🎤🤖