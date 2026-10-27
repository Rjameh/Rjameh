# Hi, I'm John Ameh

**Full-stack and AI engineer, Ottawa (open to remote).** I design, build and ship complete AI products end to end, across software, media, healthcare and hardware. I work AI-native: I direct AI coding agents (Claude Code), set the architecture and the rules, review every change, and let independent tools (tests, simulators, rule checkers) decide whether it works.

I have been teaching myself and building software since 2009, starting with PHP and MySQL, through a BSc and MSc in computer science and years of data work (Systems Analyst at Abbott Point of Care, SQL developer, data analytics), to the products below. That data background is why my products rest on sound data.

**All my code is in private repositories.** Each project below can be shown live, or opened to you on request: [email me to ask for access](mailto:johnameh.ca@gmail.com?subject=Access%20request%3A%20John%20Ameh%27s%20projects).

## What I build

### [PRD Executor](https://www.prdexecutor.com): live
An MCP server that turns a product spec into an ordered build plan. A coding agent runs it step by step, and each step is verified before the next one starts. It drives my other builds.
`Next.js · TypeScript · Model Context Protocol (MCP) · Firestore · Stripe`

### Futurity Engine: build plans for hardware (private, access on request)
Turns an idea for a device into a build plan (a 9-stage AI pipeline with an adversarial critic), checks every part against its maker's datasheet, simulates the circuits, and generates KiCad circuit boards that pass KiCad's own rule checks. On a real IoT design it caught an undersized power filter, a missing mains fuse and ten parts the plan had left out.
`Next.js · TypeScript · Python · KiCad · ngspice`

### GPU Bottleneck Agent (private, access on request)
A local command-line tool that finds the slowest part of a PyTorch program on an NVIDIA GPU, tries fixes on a copy, and proves each result: outputs checked against the original, before-and-after timing with a statistical test. A fix that is slower or changes the results is reported, never hidden. Built from a 430-step plan; all steps done.
`Python · PyTorch · CUDA`

### VidSolve Studio: AI film, book and video production (private, access on request)
One app from idea to finished film, book or YouTube video: writing, pictures, voice, editing and upload. Every paid AI call is priced and approved first: a 64,000-word novel cost $8.92 in total. Keeps a 529-shot storyboard in step with script rewrites.
`Next.js · TypeScript · PostgreSQL/Drizzle · Claude, Gemini · Veo · ElevenLabs · FFmpeg`

### Clicked: learn any codebase (private, access on request)
Teaches a codebase from a knowledge graph: walkthroughs, quizzes, beginner guides checked against a real run, and how the project was built from its git history. Lifted lesson accuracy from about 79% to about 95% on 600+ functions.
`TypeScript · TypeScript Compiler API · Node/Express · PostgreSQL · D3`

### mentacare: privacy-first clinical platform (private, access on request)
Consent-gated intake, ASRS assessments and AI-assisted reports. Personal details are removed (Microsoft Presidio) before any AI sees them. MFA, audit log, Stripe billing.
`Next.js · Supabase · Python (Presidio) · Stripe`

### Also (private, access on request)
- **IASA**: Go auto-scaling system with a live dashboard.
- **Complyant**: compliance platform: NestJS pnpm monorepo, Redis/BullMQ, WorkOS, AWS CDK.
- **DataGuard**: AI agents that monitor and repair data pipelines; CI with end-to-end tests.
- **In progress:** Scriptorium (research and script-writing agents with a review board of critics), Fayton (learning engine), ReceiptRadar (personal spending tool).

## How I work
Trace before patching. Let independent tools judge the result, not the AI: tests, simulators, datasheets, rule checkers. Prove a check works by watching it fail when it should. Price every paid AI call before it runs. Say plainly what is solid and what is not.

## Education
MSc Advanced Computer Science (data science focus), University of Reading · BSc (Hons) Computer Science, University of Jos · Microsoft Certified: Azure AI Fundamentals

## Reach me
johnameh.ca@gmail.com · [LinkedIn](https://www.linkedin.com/in/johnameh) · [prdexecutor.com](https://www.prdexecutor.com) · Ottawa, Canada
