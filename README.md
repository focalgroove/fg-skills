# FocalGroove Skills

Agent skills for AI coding agents from Focal Groove.

## Install

```bash
npx skills add focalgroove/fg-skills
```

To install a specific skill:

```bash
npx skills add focalgroove/fg-skills --skill humanize-the-copy
```

Works with Claude Code, Cursor, GitHub Copilot, Cline, and [many more agents](https://skills.sh).

## Claude app and Cowork

For [Claude app](https://claude.ai) chats or Cowork, upload a skill as a ZIP (or `.skill` file — same format). Package from the repo root so the archive contains the skill folder, not loose files:

```bash
cd skills
zip -r ../humanize-the-copy.skill humanize-the-copy/
```

Then in Claude: **Settings → Capabilities → Skills → Upload skill**, select `humanize-the-copy.skill`, and toggle it on.

The source of truth in this repo is `skills/<name>/SKILL.md`. You do not need to commit a `.skill` file — build it when you need to upload. Coding agents should use `npx skills add` above instead.

**Note:** Claude app limits the `description` in frontmatter to about 200 characters. The skills in this repo use longer descriptions for coding agents; trim the description in a copy if Claude rejects the upload.

## Available Skills

### humanize-the-copy

Clean AI-generated or AI-suspected writing so it reads more natural, direct, and human. Removes em dashes, LLM tropes, corporate filler, formulaic openings, repetitive transitions, and markdown-heavy formatting.

**Use when:**

- Asked to "humanize the copy," "de-AI this," or "make this sound human"
- Cleaning up AI-drafted content before publishing
- Removing obvious AI writing tells from any text
