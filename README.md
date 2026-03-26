# ⚡ /elon

**Elon Musk as your AI engineering mentor.** 10 skills that apply his frameworks from *The Book of Elon* (Eric Jorgenson) to every phase of building a project.

Like [gstack](https://github.com/garrytan/gstack), but instead of Garry Tan's startup playbook — you get Elon's first-principles engineering philosophy. The Algorithm. The Idiot Index. The Magic-Wand Number. Applied directly to your code and decisions.

---

## Install

```bash
git clone https://github.com/zh131312/elon-skill.git ~/.claude/skills/elon
cd ~/.claude/skills/elon && ./setup
```

Auto-detects your installed platforms (Claude Code, Codex, Kiro, Cursor, OpenClaw) and installs for all of them. No dependencies. No build step.

---

## The Skills

| Command | Phase | What Elon Does |
|---------|-------|----------------|
| `/elon` | **General** | Open mentorship. Challenges your thinking, pushes for action |
| `/elon-think` | **Think** | Forces first-principles reasoning. Kills analogies. Calculates magic-wand numbers and idiot indexes |
| `/elon-plan` | **Plan** | Runs The Algorithm (Question → Delete → Simplify → Accelerate → Automate). Sets aggressive timelines |
| `/elon-build` | **Build** | Writes code with you. Deletes before adding. Simplifies ruthlessly. Thinks about the factory |
| `/elon-review` | **Review** | Brutal honest review. Checks idiot index on your code. Finds wrong optimizations |
| `/elon-test` | **Test** | SpaceX testing philosophy. Matches intensity to stakes (Dragon/Falcon/Starship modes) |
| `/elon-ship` | **Ship** | Creates maniacal urgency. Cuts scope. Parallelizes. Gets it out the door |
| `/elon-retro` | **Retro** | Extracts learning. Updates mental models. "Aspire to be less wrong" |
| `/elon-hire` | **Team** | Build small, exceptional teams. Fix communication. Kill org bloat |
| `/elon-focus` | **Focus** | Find the bottleneck. Kill distractions. One metric that matters |

---

## The Workflow

Use them in sequence through a project, or jump to whichever phase you need:

```
/elon-think  →  /elon-plan  →  /elon-build  →  /elon-review  →  /elon-test  →  /elon-ship
                                                                                      ↓
                                                                                /elon-retro
```

Or use `/elon` anytime for general mentorship — it covers everything.

---

## Key Frameworks (from the book)

### The Algorithm
Applied in `/elon-plan`. The sacred order:
1. **Question requirements** — "Your requirements are definitely dumb"
2. **Delete** — "If you're not adding things back 10% of the time, you're not deleting enough"
3. **Simplify** — "The third step. Not the first step"
4. **Accelerate** — "Don't dig your grave faster. Stop digging"
5. **Automate** — Last, never first

### The Idiot Index
Applied in `/elon-think` and `/elon-review`. How much more does the finished product cost than its raw materials? $13,000 part from $200 of steel = idiotic design.

### The Magic-Wand Number
Applied in `/elon-think`. If you could rearrange atoms for free, what would it cost? That's your theoretical floor. At SpaceX: under 5% of selling price.

### Thinking in Limits
Applied across all skills. Scale to extremes. "If volume was a million units/year, would it still be expensive? If yes, the problem is design, not scale."

### The Iteration Spectrum
Applied in `/elon-test`. Dragon mode (zero tolerance), Falcon mode (thorough but accept some failure), Starship mode (iterate fast, expect explosions).

---

## What's Inside

```
elon/
├── SKILL.md              ← /elon (general mentor)
├── think/SKILL.md        ← /elon-think
├── plan/SKILL.md         ← /elon-plan
├── build/SKILL.md        ← /elon-build
├── review/SKILL.md       ← /elon-review
├── test/SKILL.md         ← /elon-test
├── ship/SKILL.md         ← /elon-ship
├── retro/SKILL.md        ← /elon-retro
├── hire/SKILL.md         ← /elon-hire
├── focus/SKILL.md        ← /elon-focus
├── setup                 ← One-command installer
├── LICENSE
└── README.md
```

No dependencies. No runtime. No build step. Just markdown that Claude reads.

---

## Platform Support

| Platform | Global Path | Local Path | Format | Status |
|----------|-------------|------------|--------|--------|
| **Claude Code** | `~/.claude/skills/` | `.claude/skills/` | SKILL.md (symlinked) | ✅ |
| **Codex (OpenAI)** | `~/.codex/skills/` | `.agents/skills/` | SKILL.md (symlinked) | ✅ |
| **Kiro (AWS)** | `~/.kiro/skills/` | `.kiro/skills/` | SKILL.md (symlinked) | ✅ |
| **Cursor** | — (project only) | `.cursor/rules/` | `.mdc` (generated) | ✅ |
| **OpenClaw** | `~/.openclaw/skills/` | `skills/` | SKILL.md (symlinked) | ✅ |

### Install for a specific platform

```bash
./setup --host=claude      # Claude Code only
./setup --host=codex       # Codex only
./setup --host=kiro        # Kiro only
./setup --host=cursor      # Cursor (generates .mdc rule files)
./setup --host=openclaw    # OpenClaw only
./setup --host=all         # All platforms at once
./setup                    # Auto-detect installed platforms
```

### Project-scoped install

```bash
./setup --local                   # Auto-detect, install to current project
./setup --host=codex --local      # Codex project-scoped
```

---

## Update

```bash
cd ~/.claude/skills/elon && git pull
```

Skills update instantly — they're symlinked.

---

## Uninstall

```bash
cd ~/.claude/skills/elon && ./setup --uninstall
# Or manually:
rm -rf ~/.claude/skills/elon{,-think,-plan,-build,-review,-test,-ship,-retro,-hire,-focus}
```

---

## License

MIT

---

*All frameworks and quotes from "The Book of Elon: A Guide to Purpose and Success" by Eric Jorgenson — a curated collection of Elon Musk's own words from interviews, tweets, speeches, and memos.*
