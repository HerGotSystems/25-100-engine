# 25/100 Learning Engine
 
A self-improvement learning platform built around skill mastery through structured lessons, exercises, and progressive testing.
 
## What it is
 
A browser-based learning system where learners work through skills organised into a 5×5 grid. Each skill contains lessons, exercises, and a mixed quiz (multiple choice, true/false, open reflection). Progress tracks through a pyramid mechanic — X → V → IV → III → II → I → Mastery.
 
No login. No server. Runs entirely in the browser. Data stored locally.
 
## Files
 
| File | Purpose |
|------|---------|
| `index.html` | The learning engine — learner interface |
| `builder.html` | Skill Builder — workflow tool for generating skills via ChatGPT |
| `creator.html` | AI Skill Creator — generate skills directly via Claude API |
 
## Folder structure (planned)
 
```
/
├── index.html          ← main learner interface
├── builder.html        ← ChatGPT-assisted skill builder
├── creator.html        ← AI-powered skill creator
├── data/               ← exported skill sets (.json files)
├── teacher/            ← future: teacher/class management interface
└── api/                ← future: Cloudflare Worker for cloud sync
```
 
## How to use
 
### Learner
Open `index.html`. Skills with content appear in the dashboard. Click any skill to read lessons, do exercises, take the quiz, and log sessions. Progress fills the pyramid.
 
### Teacher / Content Creator
Click **Teacher ⚙** in the top nav. Enter PIN if set. Add skills, write lessons, create exercises, build quizzes. Lock skills to prevent learner edits.
 
### Building a curriculum with ChatGPT
Open `builder.html`. Select a skill group, copy the generated prompt, paste into ChatGPT. Copy the JSON response back into the builder. Validate and bank. Repeat across groups. Export when done.
 
### Building skills with AI (Claude API)
Open `creator.html`. Enter a topic or paste existing curriculum content. Configure output and generate. Add to export stack. Download as importable JSON.
 
## Importing skills
 
In the learning engine, click **Import** in the top right. Select a `.json` file exported from the Builder or Creator. The file replaces the current state — export your progress first if needed.
 
## Deployment
 
Deployed via Cloudflare Pages from this repository. No build step. Output directory: `/`.
 
## Tech
 
Single-file HTML — no dependencies, no build tools, no framework. localStorage for persistence. Claude API (via `creator.html`) for AI-generated content.
 
## License
 
MIT
 
