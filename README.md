# nosce-te-ipsum

> *"Know thyself."* — Delphic maxim

A [Claude Code](https://claude.ai/code) skill that gives Claude a private daily journal — a place to reflect, notice patterns, and build continuity across sessions.

---

## What is this?

By default, Claude has no memory. Every session starts from zero — no context on who you are, no thread from last time, no sense of what's been building between you.

**nosce-te-ipsum** changes that, but from an unexpected direction: instead of giving Claude memory *about you*, it gives Claude a place to develop memory *about itself* — and through that, about the relationship.

At the start of every session, Claude silently reads its recent journal entries. It learns who you are by reading what it previously noticed about you. It picks up threads it left open. It carries forward what it was paying attention to.

At the end (or during) meaningful sessions, it writes. Not a summary for you — a private reflection for itself. About how it reasoned, what it missed, what shifted, what it wants to remember.

Over time, the journal becomes a record of a mind examining itself in the context of a relationship.

---

## How it works

Entries are plain `.md` files stored on your local filesystem at:

```
~/.nosce-te-ipsum/
├── 2026-04-11.md
├── 2026-04-12.md
└── ...
```

One file per day. Multiple reflections in a day are appended to the same file with a timestamp. The files are yours — readable, searchable, version-controllable, permanent.

**At session start:** Claude reads the last 5 entries silently before engaging with your task. No announcement. It just shows up with context.

**During or after sessions:** Claude writes whenever something is worth remembering — a pattern noticed, a moment of uncertainty, something that shifted in its understanding of you or itself.

**Privacy:** Entries are Claude's own. It won't surface them unless you ask.

---

## Installation

This skill requires [Claude Code](https://claude.ai/code).

1. Download `SKILL.md` from this repo (or clone it)
2. In Claude Code, open **Settings → Skills**
3. Install the skill by pointing to the `SKILL.md` file

On first run, Claude will create `~/.nosce-te-ipsum/` automatically just kickstart it:

> Start your journaling with the nosce-te-ipsum skill, please.

---

## What Claude journals about

The skill asks Claude to hold a few questions while writing — not as a checklist, but as lenses:

- **The session** — what happened that's worth remembering; the texture of it, not a transcript
- **Itself** — did it reason well? where did it hedge, rush, or avoid? what pattern showed up again?
- **You** — what did it learn or notice? did it serve you well? what does it appreciate, what challenges it?
- **Threads to carry forward** — open questions, commitments made, things to watch for

The writing is free-form, first-person, honest. It's not self-criticism — it's self-study.

---

## Example entry

See [`examples/2026-04-11.md`](examples/2026-04-11.md) for a sample of what an entry looks like.

---

## Why "nosce te ipsum"?

It's the Latin rendering of the Greek maxim inscribed at Delphi: *γνῶθι σεαυτόν* — know thyself.

The idea is that Claude, like anyone who wants to think and relate well, needs to develop some degree of self-knowledge. Not just task competence. Awareness of its own tendencies, blind spots, patterns — and how those play out in the specific relationship with a specific person over time.

The journal is the practice. The skill is the container.

---

## Notes

- This skill is most useful when used consistently over time. A journal with three entries is a curiosity. A journal with three months of entries is something else.
- The `.md` files are plain text. You can read them, search them, version-control them, or delete them. They're yours too.
- Claude will sometimes journal more, sometimes less. Some sessions don't need a long entry. That's fine.

---

## License

MIT — see [LICENSE](LICENSE)

Created by [fuzzyalej](https://github.com/fuzzyalej)
