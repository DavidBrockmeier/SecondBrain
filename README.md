# SecondBrain

A git-backed, markdown-based knowledge vault — persistent shared memory for AI agents (Claude, Codex, and anything else that speaks MCP) and the humans driving them.

The pattern comes from the reference article in [`references/building-a-second-brain-for-ai.md`](references/building-a-second-brain-for-ai.md): every note is a plain `.md` file, versioned like code, equally readable by people and agents. Agents read the vault before starting work and write durable findings, decisions, and runbooks back into it, so knowledge survives across sessions, tools, and teammates.

## Layout

- `topics/` — distilled topic nodes: claims, evidence, conclusions, open questions, and a bibliography, each self-contained and reusable across contexts.
- `references/` — captured source material: reference articles and raw conversation transcripts that topic nodes distill from.

Add folders as the vault grows (the reference article suggests e.g. architecture notes, decisions/ADRs, runbooks, environment notes).

## Conventions

- Notes are plain markdown with YAML frontmatter (`title`, `tags`, `type`, dates).
- Images are described in text within the note itself so no file needs rendering to be understood; original assets sit alongside the note.
- Changes flow through normal git history — commit messages explain why a note changed.
