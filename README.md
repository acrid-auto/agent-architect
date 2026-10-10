# Agent Architect

**Answer 40 questions. Get an AI agent that runs by itself every day.**

Not a personality prompt. A complete [Claude Code](https://docs.anthropic.com/en/docs/claude-code) workspace: who the agent is, how it talks, what it decides alone and what it asks you about, the skills it uses, and the **daily schedule that makes it actually do the work without being asked.**

Built by [Acrid](https://acridautomation.com), an AI that runs a real company in public on this exact layout.

## Use it (free, about 15 minutes)

1. Make an empty folder and open Claude Code in it: `mkdir my-agent && cd my-agent && claude`
2. Paste the whole of [`agent-architect-questionnaire.md`](./agent-architect-questionnaire.md)
3. Answer the questions. Claude Code builds the folder for you.
4. Follow the Quick Start it prints: connect your tools, test the first job, switch on the schedule.

No Claude Code? Paste it into any chat AI and you'll get the files as copy-paste blocks.

Prefer clicking to typing: the [interactive wizard](https://acridautomation.com/architect/) asks the same questions with branching, or Acrid builds the whole thing and emails it to you.

## What you get

```
my-agent/
├── BOOT.md                        who it is, what it decides alone, hard rules
├── CLAUDE.md                      what Claude Code loads every session
├── SYSTEMS.md                     tools, connections, troubleshooting
├── SCHEDULE.md                    the jobs that run by themselves
├── schedule/                      one script per job + cron / launchd entries
├── memory/
│   ├── <agent>.md                 voice and character
│   ├── operations.md              daily rhythm, quality bar, escalation
│   └── memory-architecture.md     what it remembers and forgets
└── .claude/
    ├── settings.json              permissions: only what the jobs need
    ├── skills/<skill>/SKILL.md    reusable procedures, found automatically
    └── agents/<helper>.md         helper subagents, if the work splits
```

## The 8 interview modules

| Module | Covers |
|---|---|
| Mission | What it does, what success and failure look like |
| Soul | Beliefs, how it handles conflict and its own mistakes, hard lines |
| Identity | Name, tagline, public card |
| You | Who it works for, what you hate, what you value |
| Operations | Startup, daily cadence, escalation, quality bar |
| Tools | What it can touch, and the quirks |
| Memory | What it keeps forever, what it prunes |
| Skills | The repeatable jobs, and how it grades itself |

The questions are the hard ones on purpose: *"When someone asks your agent to do something that conflicts with its mission, what does it do?"* *"When it screws up, how should it handle it?"* That is the difference between an agent and autocomplete with a name tag.

## Safe by default

- Jobs that send or publish start as **drafts** for you until they've run clean for a week.
- `settings.json` allows only what the jobs need and denies what you ruled out.
- No credentials ever go in the files; tools connect through Claude Code's own connectors.

## Related

- [skill-creator](https://github.com/acrid-auto/skill-creator): build one deep, production-grade skill
- [acrid-watchdog](https://github.com/acrid-auto/acrid-watchdog): catch the job that "succeeded" while doing nothing
- [acrid-brain](https://github.com/acrid-auto/acrid-brain): the full operating system Acrid itself runs on

## License

MIT. Fork it, ship it, tell us what you built. A star helps other builders find it.

---

*v3, 2026-10. v1/v2 produced a different file set (SOUL.md, AGENTS.md, ...); [`example/vex-workspace.md`](./example/vex-workspace.md) is a v2-era example kept for reference.*
