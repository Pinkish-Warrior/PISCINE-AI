# AI.GO — Technical Setup

One-time setup for the whole roadmap ([`WORKFLOW.md`](WORKFLOW.md)). The curriculum is plain HTML/CSS/JavaScript — no build tools, no package.json, nothing to compile. Do this once before Step 1; every step after that reuses the same environment.

Pick the path that matches where you're working:

- **[Option A — Your own machine](#option-a--your-own-machine)** — install everything yourself, once.
- **[Option B — College machine](#option-b--college-machine)** — log in and go, tools are already installed.

---

## Option A — Your own machine

### 1. Install a code editor

[Download VS Code](https://code.visualstudio.com/) and install it.

Verify from the terminal:
```bash
code --version
```
(If `code` isn't found, open VS Code → Cmd+Shift+P → "Shell Command: Install 'code' command in PATH".)

### 2. Install Git

- **macOS:** `brew install git` (or it may already be installed — check first)
- **Windows:** [git-scm.com](https://git-scm.com/downloads)
- **Linux:** `sudo apt install git` / your distro's package manager

Verify:
```bash
git --version
```

### 3. Clone the exercises repo

```bash
git clone https://github.com/01-edu/public.git
cd public/subjects/AI.GO
code .
```

### 4. Sign up for an AI assistant

Every exercise README ends with a **Prompt Example** — a suggested prompt for an AI assistant to help when you're stuck (this is the "AI" in AI.GO). Create an account with one:

- [claude.ai](https://claude.ai)
- [chatgpt.com](https://chatgpt.com)

Optional but recommended: an in-editor AI extension (e.g. Claude Code, GitHub Copilot) so you can prompt without leaving VS Code.

### 5. Running your code from the terminal

No npm install, no dev server required by the curriculum — but opening HTML files directly (`file://`) can silently break things like `fetch` or ES modules in later exercises, so serving over `http://` is safer.

**Just open the file (fine for early, simple exercises):**
```bash
open index.html        # macOS
```

**Serve it locally (recommended):**

Requires [Node.js](https://nodejs.org) installed once, then from inside an exercise folder:
```bash
npx serve .
```
Open the printed `http://localhost:...` URL in your browser. Leave this running in a terminal tab; it auto-reloads on refresh (not hot-reload — you still need to save + refresh the browser).

---

## Option B — College machine

The college machines already have VS Code, Git, and Node.js installed — you're just logging in and cloning the repo.

### 1. Log in

- **Username:** `student`
- **Password:** `student`

### 2. Verify the tools are there

Should already be installed — this is just a quick check before you rely on them:

```bash
code --version
git --version
node --version
```

If any of these fail, install the missing one following the [Option A steps](#option-a--your-own-machine) for that tool, then continue below.

### 3. Open a terminal and clone the exercises repo

```bash
git clone https://github.com/01-edu/public.git
cd public/subjects/AI.GO
code .
```

### 4. Sign up for an AI assistant

Same as Option A — every exercise README ends with a **Prompt Example**. Create an account with one:

- [claude.ai](https://claude.ai)
- [chatgpt.com](https://chatgpt.com)

### 5. Running your code

```bash
npx serve .
```
Open the printed `http://localhost:...` URL in the browser.

> Working on a shared machine: don't leave yourself logged into personal accounts (AI assistant, Gitea) at the end of a session, and confirm whether your clone of `your repo` should be pushed somewhere or is expected to be wiped between sessions.

---

## Verify your setup

- [ ] `code --version` prints a version
- [ ] `git --version` prints a version
- [ ] `public/subjects/AI.GO` exists locally after cloning
- [ ] AI assistant account created
- [ ] `npx serve .` (or opening `index.html`) shows a page in the browser

Once all boxes are checked, start at Step 1 (`first-hello`) in [`WORKFLOW.md`](WORKFLOW.md) — task instructions live in [`01-edu/public/subjects/AI.GO/first-hello`](https://github.com/01-edu/public/tree/master/subjects/AI.GO/first-hello).
