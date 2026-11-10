# First-Time Local Setup

This guide is for people who are completely new to this repo and want to run it locally without already knowing the Claude Code workflow.

## What this repo is

This is an AI-assisted job search workspace. It helps you:
- set up your candidate profile
- search for jobs
- evaluate fit
- draft CVs and cover letters
- prepare for interviews

## What you need first

### 1) Clone the repo

If you do not have it yet, clone the repository and open the project folder.

### 2) Install the job-search tools

Follow the setup instructions in the README and install the portal tools with Bun.

If you are on macOS or Linux, the common pattern is:
- go into each tool folder under `.agents/skills/.../cli`
- run `bun install`

The repo already ships with search tools such as:
- `linkedin-search`
- `freehire-search`
- Danish portal tools like Jobindex, Jobbank, Jobnet, and Jobdanmark

### 3) Install Claude Code

This repo is driven by Claude Code.

If the `claude` command is missing, install it globally:

```bash
npm install -g @anthropic-ai/claude-code
```

Then verify it works:

```bash
claude --version
```

If `claude` is still not found after installation, open a new terminal session and try again.

## First run

### 4) Start Claude Code from the repo root

From the repository root, run:

```bash
claude
```

If you are in the wrong directory, move into the repo first:

```bash
cd /Users/kshitijdarekar/Development/ai-job/ai-job-search
```

### 5) Run setup

Inside Claude Code, type:

```text
/setup
```

That starts onboarding.

## Choose one setup path

### Path A: Documents folder
Best if you already have a CV, LinkedIn export, diplomas, or reference letters.

Put your files in:
- `documents/cv/`
- `documents/linkedin/`
- `documents/diplomas/`
- `documents/references/`

Then run `/setup`.

### Path B: Single CV import
Best if you only have one CV/resume file.

Paste it or attach it when Claude asks.

### Path C: Interview mode
Best if you are starting from scratch.

Claude will ask structured questions about:
- identity and contact details
- education
- experience
- skills
- behavioral style
- career goals
- job search preferences

## What happens after setup

After onboarding, the usual flow is:
1. `/scrape` to search jobs
2. `/rank` to score results
3. `/apply` to create tailored documents
4. `/interview` to prepare for meetings

## Common beginner issues

### `claude: command not found`
Install Claude Code with:

```bash
npm install -g @anthropic-ai/claude-code
```

Then reopen the terminal.

### `claude` opens in the wrong folder
Make sure you are inside the repo root before starting Claude Code.

### Job tools do not run
Re-check that you ran `bun install` inside each tool folder under `.agents/skills/`.

## Do I need Copilot?

No. This repo can be used with Claude Code and the local tools only.

## Do I need a paid subscription?

The repo itself is free.

What you may need for Claude Code is either:
- an Anthropic API key, or
- a Claude Pro/Team subscription

The job-search tools in this repo do not require a separate paid subscription.

## Short version

If you want the fastest path:
1. Install Bun tools
2. Install Claude Code
3. Run `claude`
4. Type `/setup`
5. Pick Path A, B, or C

