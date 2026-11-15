# Hi, I'm John Ameh

**Full-stack and AI engineer, Ottawa (open to remote).** I design, build and ship complete AI products end to end, across software, media, healthcare and hardware. I work AI-native: I direct AI coding agents (Claude Code), set the architecture and the rules, review every change, and let independent tools (tests, simulators, rule checkers) decide whether it works.

I have been teaching myself and building software since 2009, starting with PHP and MySQL, through a BSc and MSc in computer science and years of data work (Systems Analyst at Abbott Point of Care, SQL developer, data analytics), to the products below. That data background is why my products rest on sound data.

**All my code is in private repositories.** Each project below can be shown live, or opened to you on request: [email me to ask for access](mailto:johnameh.ca@gmail.com?subject=Access%20request%3A%20John%20Ameh%27s%20projects).

Several recent projects were each made for one Anthropic job listing. For those, the role is named, and "mock mode" means Claude's replies were replayed from saved files, not called live.

## Tools that build tools

### [PRD Executor](https://www.prdexecutor.com): live
An MCP server that turns a product spec into an ordered build plan. A coding agent runs it step by step, and each step is verified before the next one starts. It also hands the agent house rules and skill files, and gives every prototype screen its own build stage. Most of the projects below were built through it, stage by stage.
`Next.js · TypeScript · Model Context Protocol (MCP) · Firestore · Stripe`

### Prototype Studio: from one landing page to a full clickable prototype
Four Claude skills (design system, page patterns, clickable prototype, page review). They start from one landing page designed in Google Stitch and build the whole app as one clickable HTML file. Automatic checks make sure every page fits one screen and every link works. Each built app is then checked screen by screen against these pictures.
**Status:** in use; it made the prototypes for BioLit Connect, Incident Desk, CyberCoach Bench, Dispatch Desk, Site Walk and Fault Line.
`Claude skills · Python · Node · Google Stitch`

### Clicked: learn any codebase
Teaches a codebase from a knowledge graph: walkthroughs, quizzes, beginner guides checked against a real run, and how the project was built from its git history. Lifted lesson accuracy from about 79% to about 95% on 600+ functions.
`TypeScript · TypeScript Compiler API · Node/Express · PostgreSQL · D3`

## AI agents and evaluation

### BioLit Connect: biomedical answers where every claim is checked
An agent searches PubMed, Europe PMC, UniProt and PubChem through four MCP tools and writes an answer made of claims. Each claim points to an exact sentence in a paper, and a second, separate model call checks that the sentence really supports it. A 40-question benchmark measures answer and citation accuracy.
**Made for:** Applied AI Engineer, Beneficial Deployments (Life Sciences). **Status:** rebuilt end to end through PRD Executor: 81 steps, 838 backend tests, 45 browser tests, all 19 screens checked against its prototype. Mock mode so far; the benchmark has not yet run on a live model.
`Python · FastAPI · MCP · SQLAlchemy · PostgreSQL · Next.js · Playwright`

### Agent Eval Lab: fair tests for coding agents
Researchers write coding tasks with hidden tests, run agent setups in isolated Docker sandboxes, get blind reviews from people, and compare results with statistics. It answers three questions: which setup passes more tasks, which failures are common, and whether an agent's confidence predicts its test result.
**Status:** built through all 155 steps of its PRD Executor plan, then reworked page by page to match its prototype. A CI smoke test builds the full stack; there is no deploy target yet.
`Next.js · TypeScript · FastAPI · PostgreSQL · Docker · SciPy/statsmodels`

### Injection Gauntlet: prompt-injection test lab
A command-line lab that measures how well defences stop hidden instructions in web pages, emails and files from taking over a tool-using agent. Tools are simulated, so no attack can reach the outside world. It compares a stricter prompt, a checker model and a trained classifier, with 95% ranges, and any run can be repeated with one command.
**Made for:** Anthropic Fellows Program, AI Safety & Security. **Status:** built end to end through PRD Executor: 22 stages, 374 tests (94.97% coverage), 300 cases (240 attacks, 60 clean tasks). Every result so far comes from a scripted stand-in model; nothing has been measured on Claude yet.
`Python · Click · PyTorch · Hugging Face Transformers · SQLite · pandas`

### CyberCoach Bench: security task tests and team playbooks
Tests what Claude can do on security work: find a flaw, triage an alert, write a detection rule, map an incident to MITRE ATT&CK, and attack a deliberately weak app. Success rules are written before each run, and graders check that a detection rule catches the attack and stays quiet on normal logs. Attack steps can only reach the local lab. Results become dated customer playbooks that go stale after a model update.
**Made for:** Manager, Applied AI Cyber Specialists. **Status:** built end to end through PRD Executor: 25 stages, 210 API tests, grader coverage 98%, all 14 screens checked against its prototype. Mock mode so far.
`Next.js · TypeScript · FastAPI · PostgreSQL · Docker (OWASP Juice Shop) · Sigma`

### Dispatch Desk: an agent for late, damaged or lost shipments
The agent reads each exception, looks up the shipment and the customer's contract, and proposes the next step. Any step that costs money waits for a person to approve it. A Java adapter lets the agent work next to an older system without changing it, and a 150-case evaluation set shows accuracy by exception type.
**Made for:** Forward Deployed Engineer. **Status:** built end to end through PRD Executor: 24 stages, 134 API tests, all 15 screens checked against its prototype. Mock mode so far; the Java adapter has not yet been proven running live.
`Next.js · TypeScript · FastAPI · Java 21 Spring Boot · MCP · PostgreSQL`

## Operations and reliability

### Incident Desk: incident response coordination
Runs the human side of an incident: severity from editable rules, paging from a rota, a live timeline of every decision, and reminders when an update is overdue or no owner is named. Claude drafts updates for leaders, customers or the status page; a check flags any number or time that is not in the timeline, and nothing is sent until a person presses Send. After the incident it drafts a blameless review and keeps chasing open action items.
**Made for:** Incident Response Manager, Product & Engineering. **Status:** built end to end through PRD Executor: 22 stages, 241 API tests (96.9% line coverage), all 16 screens checked against its prototype. Mock mode so far; Slack, PagerDuty and Jira use local stand-ins.
`Next.js · TypeScript · FastAPI · PostgreSQL · Redis · WebSockets`

### GPU Bottleneck Agent
A local command-line tool that finds the slowest part of a PyTorch program on an NVIDIA GPU, tries fixes on a copy, and proves each result: outputs checked against the original, before-and-after timing with a statistical test. A fix that is slower or changes the results is reported, never hidden. Built from a 430-step plan; all steps done.
`Python · PyTorch · CUDA`

### Site Walk: field engineer issue and decision log
A phone-first app for data center construction sites. Issues are pinned to the floor plan with photos, driven to a decision with an owner and a date, and flagged for escalation when a date slips twice. It works offline on site and syncs later, and a trend page turns repeating problems into changes to design checklists.
**Made for:** Field Engineer, Data Center Design and Engineering. **Status:** built end to end through PRD Executor: 15 stages, 102 API and security tests (92.8% coverage), offline journey test passes, all 19 screens checked against its prototype. Not yet tried on real phones.
`Next.js (installable, offline) · FastAPI · PostgreSQL/pgvector · MinIO · IndexedDB`

### Fault Line: evidence-first incident diagnosis
When an alert fires, it lines up every change in the time window (deploys, config, certificates, infrastructure) and builds competing explanations. Each one shows the evidence for and against, a confidence score and the one check that would settle it. A fault injector on a demo system will measure how often the true cause is ranked first.
**Made for:** Staff+ Software Engineer, Observability. **Status:** prototype done (21 screens); build plan being generated; not built yet.
`Next.js · FastAPI · PostgreSQL · Redis · OpenTelemetry · Prometheus, Loki, Tempo, Pyroscope`

## AI products in other fields

### Futurity Engine: build plans for hardware
Turns an idea for a device into a build plan (a 9-stage AI pipeline with an adversarial critic), checks every part against its maker's datasheet, simulates the circuits, and generates KiCad circuit boards that pass KiCad's own rule checks. On a real IoT design it caught an undersized power filter, a missing mains fuse and ten parts the plan had left out.
`Next.js · TypeScript · Python · KiCad · ngspice`

### VidSolve Studio: AI film, book and video production
One app from idea to finished film, book or YouTube video: writing, pictures, voice, editing and upload. Every paid AI call is priced and approved first: a 64,000-word novel cost $8.92 in total. Keeps a 529-shot storyboard in step with script rewrites.
`Next.js · TypeScript · PostgreSQL/Drizzle · Claude, Gemini · Veo · ElevenLabs · FFmpeg`

### ML Engine: from a business question to a released model
Upload, profiling, training, scoring and release are all done for real. Every compute spend needs an approved cap, and a run stops itself before it would pass it. The holdout set is scored once, release needs a sign-off, and a drift check compares new data with the training data.
**Status:** built through all 60 steps of its PRD Executor plan; a browser test walks the whole journey and checks all 16 screens against its prototype.
`Next.js · TypeScript · FastAPI · DuckDB · scikit-learn · LightGBM · Playwright`

### mentacare: privacy-first clinical platform
Consent-gated intake, ASRS assessments and AI-assisted reports. Personal details are removed (Microsoft Presidio) before any AI sees them. MFA, audit log, Stripe billing.
`Next.js · Supabase · Python (Presidio) · Stripe`

### Also
- **IASA**: Go auto-scaling system with a live dashboard.
- **Complyant**: compliance platform: NestJS pnpm monorepo, Redis/BullMQ, WorkOS, AWS CDK.
- **DataGuard**: AI agents that monitor and repair data pipelines; CI with end-to-end tests.
- **In progress:** Scriptorium (research and script-writing agents with a review board of critics), Fayton (learning engine), ReceiptRadar (personal spending tool).

## How I work
Trace before patching. Let independent tools judge the result, not the AI: tests, simulators, datasheets, rule checkers. Prove a check works by watching it fail when it should. Price every paid AI call before it runs. Say plainly what is solid and what is not.

## Education
BSc Computer Science · MSc Computer Science

## Reach me
johnameh.ca@gmail.com · [LinkedIn](https://www.linkedin.com/in/johnameh) · [prdexecutor.com](https://www.prdexecutor.com) · Ottawa, Canada
