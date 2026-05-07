# PM AI Skills Workshop Skeleton

## Overview

A hands-on workshop walking Kueski PMs through the full AI-assisted product workflow — from problem definition to a shipped pull request — using AI tools and the Kueski PM skill suite.

**Ultimate goal:** PMs can take an idea from their head to a full brief, prototype and develpment.

**PM Pre-req**:

* Access to Cursor, Codex or Claude
* Access to github
* Access to repos owned by your domain

---

## Day 1 — Monday (approx. 3:30–6pm, after business metrics session)

---

### Module 1: The AI Landscape & Your Toolkit (45 min)

**Goal:** Everyone understands what tool to use when, and can find their way around Claude Code.

#### Topics

* **The AI Landscape: Chat vs. Code vs. Cowork** — what's the difference, and when to use what.

  **💬 Chat** *(Claude.ai, ChatGPT)*
  - Conversational, one-off, no setup
  - Lives in your browser — paste in, get answer, done
  - **Use when:** you want something quick and disposable
    - Drafting a Slack message or email
    - Improving your writing
    - Asking a quick question or explaining a concept
    - Brainstorming before you've committed to anything

  **⌨️ Code** *(Claude Code, Cursor, Codex)*
  - The most powerful mode — Claude with hands
  - Reads files, runs commands, connects to tools (Jira, GitHub, Databricks)
  - **Use when:** you want to go end-to-end on something real
    - Idea → brief → Jira tickets → prototype → PR
    - Running the Kueski PM skill suite ← **this is what we're using this week**
  - Pick whichever you have set up: Claude Code, Cursor, or Codex — the skills work the same across all three

  **🤝 Cowork**
  - A structured UI built on top of Code — same engine, friendlier interface
  - Best for repeatable, scheduled workflows
  - **Use when:** you have a routine you want to automate
    - "Summarize my unread emails every morning at 8am"
    - "Flag my Jira tickets with no updates this week every Friday"
    - Everything Cowork can do, Code can also do — it's just a different interface

* **Claude vs. ChatGPT vs. Cursor — Different doors, same destination**

  **Claude** *(Anthropic)*
  - **Web / App** → claude.ai — this is the Chat version, browser or desktop app
  - **Claude Code** → lives in your terminal. You open it by typing `claude` in your command line. This is the Code version.

  **ChatGPT / Codex** *(OpenAI)*
  - **Web / App** → chatgpt.com — the Chat version
  - **Codex** → accessible as a VS Code extension or via the OpenAI API. Sits inside your editor.

  **Cursor**
  - **Desktop app only** → cursor.com. Looks like VS Code but with AI baked in everywhere — you pick which model powers it (Claude, GPT-4, etc.).

  **For this workshop:**
  Pick the one you already have open. Claude Code, Codex, and Cursor all run the Kueski skill suite the same way. If you're not sure which to use, default to Claude Code — we'll move on now and you can always switch later.
* **What is a markdown file** — why markdown is the preferred format for working with AI (most accurate, cheapest), how to read and write basic markdown, why your briefs and notes should live in `.md` files
* **GitHub basics** — one mental model only: think of it as Google Drive for code. Repos, branches, files — just enough to not be lost during setup
  * Same idea, different object: Google Drive holds documents you collaborate on. GitHub holds code the team builds and ships. The habits feel familiar; the "documents" are mostly text files written in programming languages instead of natural language.
  * Folders → repositories (repos): In Drive you organize work in folders (and shared drives). In GitHub the top-level "place" for one product or service is usually a repository — one box that holds that project's files, history, and collaboration rules.
  * Named copies of the truth → branches: In Drive you might work from one canonical file, or duplicate a doc to try ideas. In GitHub teams standardize that with branches: one line of development is often called main (the current agreed-upon version), and when someone wants to change something they typically create a separate branch — a safe sandbox so main stays stable until the change is ready.
  * Files are still files: Same mental model as Drive: there are files and folders inside the repo. The difference is mostly what's inside the file — instructions for computers (code, config) rather than narrative for humans — and that small edits can have large effects, which is why review matters.
  * Suggesting mode → pull requests (PRs): In Drive, Suggesting lets you propose edits; the owner accepts or rejects them and can discuss inline. In GitHub a pull request is the same pattern at repo scale: "here is my proposed set of changes," with comments, requested changes, and approve when it's good enough to merge into the target branch (often main).
  * How that shows up for PMs at Kueski (today vs. later): When you propose a change to a file in our codebase, the workflow can include AI-assisted review (catch issues, suggest improvements), but a human still approves before it lands. Over time, as confidence in automation grows, we may rely more on AI review — but the PR idea stays the same: propose, discuss, approve, then merge.
  * Why this slide exists: You do not need to be fluent in Git commands. You need enough vocabulary — repo, branch, main, pull request, merge, approve — to follow setup, links, and "where do I put this change?" without getting lost.

---

### Module 2: Skills (60 min)

**Goal:** Build the mental model for skills and develop judgment for when to use AI vs. human thinking.

[https://github.com/kueski-dev/claude_agent_skills](https://github.com/kueski-dev/claude_agent_skills)#### Topics

* What skills are and how they're triggered (`/skill-name`)
* How to list available skills and read what a skill does
* Walk through the Kueski PM skill suite
  * what each does, when to reach for it
  * quick live demo

| Skill | When to use |
| --- | --- |
| `pm-setup` | First-time setup — builds your profile so other skills personalize output |
| `problem-definition` | Kicking off a new initiative, writing a crisp problem statement |
| `solution-brainstorm` | Before you scope — explore approaches, expand ambition |
| `data-analysis` | Back your problem statement with real Kueski data (KCash/Kpay metrics) |
| `product-director-review` | Stress-test your brief before sharing with leadership |
| `brief-jira-breakdown` | Convert a brief's requirements into Jira epics/stories |
| `brief-sync-confluence` | Keep your Confluence brief in sync with local edits |
| `eng-review` | Pressure-test technical feasibility before committing scope |
| `jira-ticket-to-pr` | Take a tagged front-end ticket → working prototype PR |

* **Human judgment vs. AI** — what AI is genuinely good at, where it falls short, how to stay in the driver's seat. What changes now: execution is cheaper, so human judgment is more important than ever

---

### Activity 1 — Setup & First Explore (rest of the day)

**Goal:** Everyone is fully set up and those who move fast get a head start on Day 2.

* Run `pm-setup` to configure your profile
* Set up connections: Atlassian, Databricks, Google Drive
* For those who finish early: pick your initiative idea and start iterating with `problem-definition`
* *No pressure to go far — getting set up cleanly is the win for today*

**Come prepared:** Think of a real initiative idea you want to develop. You'll use this tomorrow to go from raw idea to full product brief.

---

## Day 2 — Tuesday (8am–5pm)

---

### Morning: Finish the PM Workflow (8am–12pm)

#### Recap & Unblock (30 min)

* Resolve any setup issues from Day 1
* Re-orient: here's what we're building toward this morning — a full product brief

#### Activity continued — Idea → Full Brief → Prototype (2.5 hours)

**Goal:**

* Run your initiative through the full PM skills sequence and walk away with a real brief.
* Use Magic Patterns for prototype based on the brief

#### Share-out & Morning Wrap (90 min)

* 2–3 people walk through their brief: the idea, what the skills helped with, what they pushed back on, what’s not working
* Group reflection: where did you use human judgment? Where did AI surprise you?
* What would the next step be if this were a real initiative?

---

*Lunch (12–1pm)*

---

### Afternoon: How Code Ships & Your First PR (1–5pm)

---

### Module 3: The Code Shipping Process (45 min)

**Goal:** PMs understand how code goes from idea to production and where they fit in.

#### Topics

* How a feature travels from brief to production at Kueski
* Branches, commits, pull requests, code review, merge — explained for PMs, not engineers
* What CI/CD means in practice (you don't need to run it, but you should know it exists)
* What a good copy change ticket looks like and why it's the ideal first PR

**Notes**

# Module 3: The Code Shipping Process (45 min)

**Goal:** PMs understand how code goes from idea to production and where they fit in.

**Example repo:** `kueskipay-frontend` — the Kueski Pay consumer web app (internally also referred to as Aurora). Same ideas apply to other repos; this one is concrete.

---

## 1. Bridge from the shared language (2 min)

You already have one mental model: **GitHub is Google Drive for code** — repos, branches, files, pull requests as “suggesting mode at repo scale.” This module answers: **what happens after someone opens a PR, and how do users end up seeing the change?**

---

## 2. Quick recap — branches, commits, pull requests, review, merge

Use these terms the same way as in Module 1; here is the **shipping** angle only.

- **Branch** — A named line of work. In `kueskipay-frontend`, the line everyone eventually agrees on is **`master`** (same role as `main` in other repos; only the name differs).
- **Commit** — A saved snapshot of the files on your branch: “here is exactly what changed at this moment,” with a message. Small, frequent commits are normal; the PR is the bundle you ask others to review.
- **Pull request (PR)** — “Please pull my branch’s commits into `master`.” It shows a diff, discussion, approvals, and automated check results.
- **Code review** — Humans (and sometimes tools) read the change, comment, request edits, or **approve**. Until the team is comfortable, treat approval as the gate — same instinct as not accepting every Google Doc suggestion without reading it.
- **Merge** — When the PR is accepted, those commits become part of `master`. The shared “folder” is updated; everyone’s future work starts from that new truth.

---

## 3. What CI/CD means for a PM (plain language)

**CI (Continuous Integration)** — When you open or update a PR, **robots run in the background**: build the app, run tests, run style/security checks. You do not run these by hand on your laptop for the team to trust the change; GitHub Actions does it and posts **green or red** on the PR.

**CD (Continuous Delivery / Deployment)** — After the change is trusted and merged, **pipelines can deploy** built files to **environments** (staging first, production when the org is ready) so a URL serves the new version.

Think of CI as “automatic proof the change still works” and CD as “automatic copying of the built app to the right server / CDN bucket.”

---

## 4. What happens when you open a PR in `kueskipay-frontend`

The repo defines this in **`.github/workflows/pull_request.yml`**. It runs when a PR targets **`master`** or a **`release-*`** branch, and when the PR is opened, updated, reopened, or marked ready for review.

At a **high level** (PM-facing, not every job name):

1. **Org / governance checks** — Change management, Backstage, and CODEOWNERS-style validation run first (so the right people and catalog metadata are in place). If you are doing a small copy change with guidance, these usually pass without you thinking about them.

2. **Unit tests** — Automated tests run (with coverage expectations the team cares about). Red here means “something that used to work might be broken” — same category as “the spreadsheet formula broke,” but for the app.

3. **Build** — The app is built the way we ship it (production-style build, including bundle analysis in this workflow). Confirms the code actually compiles into deployable assets.

4. **Lint** — Style and static checks (naming, patterns, TypeScript/ESLint rules). Often the fastest feedback on small mistakes.

5. **Quality / security** — **SonarQube** runs for quality signals; **Snyk** runs for dependency and security scanning. These are “second opinions” before humans spend deep time.

6. **Version bump (automation)** — A step can propose or align version metadata from the PR context (so releases stay traceable).

**Important nuance for facilitators:** In this repo, a **normal** PM/engineering PR **does not** deploy to staging from the PR alone. The PR workflow is mostly **prove the change is safe**. **Staging deploy after merge** is the typical path (next section). There is a **special path** for certain labeled Snyk PRs that can deploy to staging and auto-merge — call it out only if the audience asks; it is not the default copy-change journey.

---

## 5. Iterate until approval

Same rhythm as a doc in **Suggesting** mode:

- Push commits to your branch → PR updates → **CI runs again** (`synchronize` events re-trigger checks).
- Fix or discuss until checks are green (or the team accepts an exception process).
- Reviewers **comment**, **request changes**, or **approve**.
- No merge until the team’s rules are satisfied (required reviewers, branch protection, etc.) — aligned with “human approves before it lands” from Module 1.

---

## 6. After merge: how it reaches **staging**

When the PR is merged into **`master`**, GitHub records new commits on `master`. That push triggers **`.github/workflows/merge_branch.yml`** (`on: push` to `master`).

Roughly, that workflow:

- Runs **lint** and **unit tests** again on the merged line.
- Runs **SonarQube** again.
- **Builds** the app (production-style build on production tooling runners).
- Runs **Snyk** again.
- **Deploys to staging** — static assets go to the staging bucket / CloudFront distribution; the staging URL documented in the workflow is **`https://kueskipay-aurora.kueski.codes/`** (internal/staging-facing Kueski Pay web).
- Runs a **performance budget** check (Lighthouse) after staging is updated.

So: **merge → automated pipeline → staging URL shows the new build.** QA and stakeholders can try the change in an environment that is not customer production.

**Depends on the repo:** What runs **after merge** (whether staging deploys at all, which branch triggers it, whether smoke tests block the pipeline) is **defined per repository** — not one global Kueski rule. The sections above describe **`kueskipay-frontend` as it is wired today**; another repo might deploy staging from the PR itself, use `main` instead of `master`, or gate production differently. When in doubt, read that repo’s `.github/workflows/` or use the prompt in **section 11** below.

---

## 7. How it reaches **production**

Production is intentionally a **stronger gate**. In this repo, **`.github/workflows/release.yml`** is triggered **manually** (`workflow_dispatch`): someone chooses a **commit** to release, optionally a **tag**, runs missing-commit validation, reuses **build artifacts** from the trusted CI paths, creates a **GitHub Release**, and **deploys to production** — target URL **`https://prod.kueskipay.com/`** (per workflow inputs).

PM takeaway: **merging to `master` does not automatically mean customers see it tomorrow.** Production is a **deliberate release** step the team schedules and owns, often with comms, support, and product readiness in mind.

---

## 8. Still “Google Drive” at the end — what the user’s browser does

Under the hood the “files” are HTML, JavaScript, CSS, and assets built from the repo. When staging or production is updated, **the CDN serves new versions of those files** (with cache rules the engineers manage).

For a PM: **users do not clone GitHub.** They open a **URL**. That URL fetches the **current published bundle** — the same mental model as opening a shared Drive link and always seeing the **latest saved version**, except the “save” was **merge + deploy**, not Cmd-S in a doc.

---

## 9. How a feature travels from brief to production (one slide of context)

Stay high level; every team’s ritual differs slightly:

- **Brief / ticket** — Problem, scope, acceptance criteria.
- **Design / eng breakdown** — What actually ships in which PRs.
- **Implementation + PRs** — Branches, CI, review, merge to `master`.
- **Staging validation** — Product, QA, or you try `kueskipay-aurora.kueski.codes`.
- **Release decision** — Manual release workflow (or org-wide release train) to `prod.kueskipay.com`.
- **Monitor** — Errors, metrics, support — same as any launch.

Your recurring seat at the table: **clear problem statement, crisp acceptance criteria, and willingness to validate on staging** — not necessarily owning the release button.

---

## 10. What a good copy-change ticket looks like (why it is the ideal first PR)

Keep this tight; Module 4 will demo and Activity 2 will practice.

**What “good” means on the ticket**

- **Be clear what the change is** — Quote the **current** and **new** copy verbatim (before/after). One string or one screen’s worth of change; avoid “make it friendlier” with no exact target text.
- **Be clear where it lives** — Name the product surface (e.g. Kueski Pay Web vs app). **On web**, use **route or URL** (e.g. `/pay/aplicar`): same precision as “open this link on staging,” and it lines up with routing and the right page in code. **On mobile**, there is no address bar — use a **tap-by-tap navigation path** from app open, **platform** (iOS / Android / both), and a **deep link** if your app supports one. Add a **screen name** that matches design if it helps people talk about it; the path + exact string are what narrow implementation fastest (including for AI search over strings and route/screen definitions).
- **Link to staging** after merge so anyone can verify (web URL; on mobile, note build/flavor if copy differs).
- **Acceptance criteria** a reviewer can tick in under a minute (“text reads X,” “no layout regression on mobile”).

**Why this shape helps AI (and humans)**

Exact copy lets search and i18n lookup land on **one or a few files** instead of guessing from a paraphrase. **Web:** path + string ties the change to the right route and page. **Mobile:** navigation path + platform reduces wrong-screen edits when the same phrase appears in two flows. Vague tickets force the model to invent scope; specific **what + where** keep the PR small and reviewable.

**Example ticket:** [PRODU-75709](https://kueski.atlassian.net/browse/PRODU-75709) — On Kueski Pay Web, on `/pay/aplicar`, change the copy from *“Primero, te pediremos algunos datos personales”* to *“Primero, necesitamos algunos datos personales.”* That is a complete mini-spec: product, URL, before, after.

**From ticket to PR (workflow you can mention, not required for the room to memorize)**

A scripted flow (`jira-ticket-to-pr PRODU-75709`) read the ticket’s acceptance-style detail, targeted `kueskipay-frontend`, and produced a concrete code change; the resulting PR is [kueskipay-frontend#1331](https://github.com/kueski-dev/kueskipay-frontend/pull/1331). The point for PMs: **tickets written like PRODU-75709** are machine- and human-friendly — clear **what** + **where** (on web, route; on mobile, navigation path and platform) means fewer round-trips and a smaller, reviewable diff.

Copy changes touch real user-facing language but usually **avoid deep logic**, so CI failures are rare and review is fast — perfect for learning the PR → merge → staging path without becoming a bottleneck.

---

## 11. Other repositories — flows differ (and a prompt for AI)

**Staging and production paths are not identical across repos.** Branch names, which event deploys staging (open PR vs merge vs manual), and how production is promoted (manual release, tag, train, or automatic) all live in that service’s CI config.

When you need the truth for **this** codebase, open the repo in your editor or GitHub and either skim **`.github/workflows/`** or paste a short prompt to your AI assistant (with the repo context attached, or the folder open in Cursor):

```
Explain in plain language (no jargon) how this repo gets to staging and production. Use exactly two bullets:
Staging — one or two short sentences on what happens and who/what triggers it.
Production — same for production.

Keep the whole answer brief enough to skim in under a minute.
```

Ask it to cite the workflow file names if you want to double-check against GitHub’s Actions tab.

---

## Facilitator notes

- **Branch name:** Say **`master`** when pointing at this repo’s GitHub UI; map it to **`main`** if the audience learned that word in Module 1.
- **If asked “where do I read this?”** — `.github/workflows/pull_request.yml`, `merge_branch.yml`, `release.yml` in `kueskipay-frontend`. AGENTS.md in that repo describes the app as Aurora and lists key commands.
- **Snyk auto path:** Only when the PR workflow’s conditional jobs run (labeled Snyk / low-risk flow). Do not present it as the default PM first PR.

---

### Module 4: Live PR Demo (30 min)

**Goal:** See the full PR process end-to-end.

* Facilitator takes a pre-seeded copy ticket and opens a PR live
* Walk through what reviewers see, the approval flow, what happens after merge
* Q&A before the activity

---

### Share-out & Close (30 min)

* Who got their PR open? Who got merged?
* What felt different about this vs. regular PM work?
* What will you use next week?

