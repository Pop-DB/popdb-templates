# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This repo hosts the **template manifest** for PopDB's `create-popdb` CLI scaffolding tool. It contains a single `templates.json` file that defines available project templates users can choose when creating a new PopDB app.

## templates.json Schema

Each template entry has:
- `id` — unique identifier used by the CLI
- `name` — human-readable display name
- `description` — shown during template selection
- `useCase` — describes when to use this template
- `techStack` — array of technologies included
- `mode` — PopDB app mode: `"webapp"` (multi-user with signup) or `"agent"` (single-user/admin tools)
- `repo` — GitHub repo path (`Pop-DB/popdb-template--<id>`) containing the actual template code

Template repos follow the naming convention `Pop-DB/popdb-template--<id>` and are pulled via `npx degit`.

## Validation

The JSON must be valid and maintain the `version` field at the top level. When adding templates, ensure the `repo` field points to an existing GitHub repo under the `Pop-DB` org.
