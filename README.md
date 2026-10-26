# ResolveAI — AI Customer Support Resolution Copilot

A portfolio-grade interactive prototype for an AI-assisted customer support product. It is intentionally designed to demonstrate product thinking as well as UI: ticket triage, human-reviewed AI drafts, source grounding, escalation, knowledge articles, product metrics, and CSV exports.

## Run the prototype
1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. Use the fictional sample tickets to explore the inbox, draft review, escalation, analytics, knowledge base, and settings.
4. All changes are local to the browser session. No customer messages are sent.

No build tools or API keys are required for the frontend demo.

## Publish on GitHub Pages
This project includes a GitHub Actions workflow that deploys the static frontend whenever changes are pushed to `main`.
1. Push the site files and workflow to the repository's `main` branch.
2. In the repository, open **Settings → Pages** and set the build and deployment source to **GitHub Actions** if it is not already selected.
3. Open the **Actions** tab and wait for **Deploy static site to GitHub Pages** to complete. The published URL will appear in the workflow run and under **Settings → Pages**.

Only `index.html` is included in the Pages deployment.

## Included features
- Support inbox with search, priority/status filters, and ticket selection
- AI-style draft responses with source snippets, confidence indicators, and risk notes
- Human approval, local resolution status, escalation, and feedback controls
- Create demo tickets and add sample knowledge articles
- Analytics overview and product measurement plan
- Export ticket data and interaction events to CSV
- Human-in-the-loop controls and explicit disabled-by-design treatment for real sending/refunds/account changes
- Responsive layout for desktop and mobile

## Important limitations
This is an interactive demo, not a production support system and not a live LLM integration. Drafts are generated from local templates and sample policies. Confidence values and dashboard examples are illustrative, not measured model performance. Data is fictional. Do not enter real customer or confidential business information.

## Recommended product case-study deliverables
1. Discovery evidence: 5–8 user interviews, problem statement, current-workflow map, and alternatives analysis.
2. PRD: target segment, jobs-to-be-done, MVP, non-goals, acceptance criteria, and risks.
3. Prioritization: RICE or another transparent framework with assumptions stated.
4. Evaluation plan: labelled ticket dataset; answer correctness, source relevance, escalation precision/recall, latency, and cost.
5. Usability test: tasks, observed friction, feedback, and iteration log.
6. Analytics: first-contact resolution, time to resolution, grounded answer rate, CSAT, escalation rate, cost per resolution.
7. Business model: target customer, pricing hypothesis, cost-to-serve, distribution, and competitive differentiation.
8. Honest results: separate simulated testing from real user pilots and never invent outcomes.

## Suggested next technical build
- Frontend: React/Next.js or keep this prototype while validating the UX
- Backend: FastAPI
- Data: PostgreSQL for tickets/events, object storage for documents
- Retrieval: embeddings + vector database, with source metadata and permissions
- LLM: provider abstraction with evaluation, timeout, retry, and cost tracking
- Observability: structured logs, prompt/version tracking, evaluation runs
- Security: authentication, role-based access, tenant isolation, data retention, audit logs, secret management
- Integrations: start with one sandbox email/helpdesk integration only after authorization and tests

## Product safety principles
- Require human approval before sending replies or taking account actions.
- Never allow an LLM to invent refund, shipping, warranty, or legal policy.
- Escalate privacy, payment, security, legal, and other high-impact issues.
- Respect access permissions when retrieving knowledge.
- Keep an audit trail for drafts, approvals, escalations, and outcomes.
