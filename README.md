# Design Client Studio

A browser-based simulator for freelance web, UI, and UX design practice.

## Start

Open `dist/index.html` in a modern browser, or serve the `dist` folder with any static web server. No build, installation, or API key is required. A fictional starter client is ready in the Client room.

Private hosted app: https://design-client-studio-rachel.petiteswan16.chatgpt.site/

## Features

- Project generation: five project types, five industries, four difficulty levels, and three scopes.
- Client role-play through discovery, scoping, design reviews, revisions, and handoff.
- Artifact links and descriptions, scope agreements, decision logs, and completion tracking.
- Separate mentor feedback for UX, UI hierarchy, accessibility, and business decisions.
- Portfolio workspace with Markdown case-study export and a self-reported evidence register.
- Browser-local persistence and JSON backup export/import. Imports preserve existing projects.

## Practice workflow

1. Ask the client about the audience, goals, budget, and constraints.
2. Move to Scoping and confirm a proposed scope.
3. Design in your preferred tool. Save an artifact link and a detailed description in Client room.
4. Request a design review. For revisions, save a second artifact, explain the changes, and explicitly request approval.
5. Use Design mentor for independent critique; mentor feedback does not change client approval.
6. Write your process and reflection in Portfolio. Add observations only from tests you actually ran, then export your case study.

## Save your work

Projects save in localStorage on the current browser and origin. They do not sync between devices or between local and hosted copies. Export backups regularly and import them when moving. Private browsing, clearing browser data, or restrictions on local files can remove or prevent persistence.

## MVP boundaries

This is a **scenario-based simulator**, not a generative AI service. Replies use topic and stage rules. Reviews and mentor prompts use text descriptions; the app cannot inspect screenshots, open design URLs, or certify accessibility. Stage navigation and completion tracking are manual.

Clients, budgets, deadlines, business constraints, and approvals are fictional. Case studies retain a concept-project disclosure. Proposed metrics remain hypotheses. Entered observations are labeled self-reported and are not independently verified. Simulated approval is not evidence of usability or business impact.

Google Fonts are optional external assets; system fonts are used when unavailable. No analytics or server-side project storage is included.

## Verify

With Node.js 18 or newer:

```sh
npm test
```

No dependency installation is needed. Checks cover JavaScript syntax and the scenario workflow: generation, discovery, scope tracking, review prerequisites, revision sign-off, mentor separation, honest export, evidence, URL filtering, and persistence. The workflow check uses a minimal DOM stub, so it is not a browser layout or end-to-end test. Visual browser QA was unavailable during the initial build.

## Structure

- `dist/`: deployable HTML, CSS, and JavaScript; edit these files directly.
- `tests/workflow.cjs`: scenario workflow checks.
- `.openai/hosting.json`: existing private Sites deployment configuration.

The application needs only static hosting. Preserve the hosting identity when updating the existing Site; use your own configuration when deploying a separate copy.
