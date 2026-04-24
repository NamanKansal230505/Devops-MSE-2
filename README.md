# DevOps MSE 2 — Submission

**Student:** Naman Kansal
**Course:** DevOps (MSE 2)
**GitHub:** [NamanKansal230505](https://github.com/NamanKansal230505)

This repository contains the solutions for all three Test Cases of the DevOps MSE 2 assignment. Each test case is organized into its own folder with the commands used and screenshots of the implementation.

---

## Repository Structure

```
Devops-MSE-2/
├── README.md
├── TestCase1/
│   ├── Commands.txt          # Linux System Audit & User Management commands
│   └── Implementation/       # Execution screenshots
├── TestCase2/
│   ├── Commands.txt          # File Permission Configuration commands
│   └── Implementation.png    # Execution screenshot
└── TestCase3/
    ├── Commands.txt          # Node.js App Setup & Git Integration commands
    └── Implementation/       # API test screenshot
```

---

## Test Case 1 — Linux System Audit & User Management

**Objective:** Perform a system audit, create groups and users, assign them to departments, and remove a user after resignation.

**Key actions performed:**
- Checked current user (`whoami`, `id`)
- Listed active sessions (`who`, `w`) and login history (`last`, `lastlog`)
- Displayed system info (`uname -a`, `hostname`, `uptime`)
- Created groups `developers` and `qa`
- Created users `aman`, `ritu` (developers), `karan` (qa)
- Removed user `ritu` along with her home directory and all active sessions

**Files:** [`TestCase1/Commands.txt`](./TestCase1/Commands.txt)

---

## Test Case 2 — File Permission Configuration

**Objective:** Create a web server file (`index.html`) and configure its ownership and permissions.

**Key actions performed:**
- Created `index.html` in the home directory with HTML content
- Viewed default permissions (`ls -l`, `stat`)
- Granted full permissions `777` (rwxrwxrwx)
- Changed ownership to `www-data:www-data`
- Applied final permissions `755` (rwxr-xr-x)

**Final verification output:**
```
-rwxr-xr-x 1 www-data www-data ... index.html
```

**Files:** [`TestCase2/Commands.txt`](./TestCase2/Commands.txt)

---

## Test Case 3 — Node.js Application Setup & Git Integration

**Objective:** Build a Node.js REST API with an Express `/health` endpoint, initialize Git, and publish it to GitHub.

**Key actions performed:**
- Initialized a Node.js project (`npm init -y`)
- Installed `express` (dependency) and `@types/express` (dev dependency)
- Created `index.js` with an Express server running on port **8080**
- Implemented `GET /health` endpoint returning HTTP 200 with `{"status":"OK"}`
- Initialized a Git repository and created the initial commit
- Pushed to a standalone public GitHub repo

**Live Node.js API Repository:** https://github.com/NamanKansal230505/nodejs-api

**Local run & verification:**
```bash
node index.js
curl http://localhost:8080/health
# Response: {"status":"OK"}
```

**Files:** [`TestCase3/Commands.txt`](./TestCase3/Commands.txt)

---

## How to Review

1. Open any `TestCase<N>/Commands.txt` to see the commands used, each with inline comments describing what they do.
2. Open the `Implementation/` folder inside each Test Case to view screenshots of the commands being executed successfully.
3. For Test Case 3, the Node.js project itself lives in its own GitHub repo (as required by the assignment): [nodejs-api](https://github.com/NamanKansal230505/nodejs-api).

---

## Submission Links

| Item | Link |
|------|------|
| Main submission repo | https://github.com/NamanKansal230505/Devops-MSE-2 |
| Node.js API repo (Test Case 3) | https://github.com/NamanKansal230505/nodejs-api |
