# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a demo/test repository integrated with Claude AI assistant. It uses `@claude` mentions in GitHub Issues and Pull Requests to trigger AI-powered tasks (code review, code modification, Q&A, etc.).

The repository is bilingual (Chinese/English).

## CI/CD

Two GitHub Actions workflows are configured in `.github/workflows/`:

- **claude.yml** — Triggers Claude Code on `@claude` mentions in issue comments, PR review comments, PR reviews, and new issues. Uses `anthropics/claude-code-action@v1`.
- **claude-code-review.yml** — Automatically runs Claude Code Review on PR events (opened, synchronized, ready_for_review, reopened) using the `code-review` plugin.

Both workflows require the `CLAUDE_CODE_OAUTH_TOKEN` secret to be configured in the repository.
