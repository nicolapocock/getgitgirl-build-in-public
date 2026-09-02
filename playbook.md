# Marketing-engineer playbook (reference)

Condensed from Greg Isenberg, "Marketing Engineer: The $1M Job with AI Agents"
(https://www.youtube.com/watch?v=8ZC1G1ezN5o). Reconciled from two independent
video reads + a human checkpoint. Load this when building out a growth OS repo past v1.

---

## The role

**Marketing engineer** (aka forward-deployed marketer / AI growth operator): the
person who **turns market signal into pipeline using AI agents, data, code, and taste**
— building a marketing system that keeps learning. The name will change; the job won't.
Claimed comp: $250K / $500K / $1M+.

Process loop: **Listen** (customer + market) → **Build** (assets + agents) →
**Ship** (content + outbound) → **Learn** (results + memory) → back to Listen.

## Tool stack (categories, not products — "the tools change, the workflow is the skill")

| Layer | Job | Named in the talk |
|---|---|---|
| Market radar | Watch the live internet, turn signal into tests | Grok Bot (close to the X ecosystem) |
| Build | Repo, scripts, landing pages, dashboards, small internal tools | Claude, Codex |
| Scheduled ops | Recurring workflows with memory + approval | Hermes-style |
| Sensitive / cheap-at-scale | Private transcripts, regulated notes, pricing | Local AI |
| Creative | Ads, thumbnails, mockups, video concepts | Fal AI, Higgsfield |

**Grok Bot lanes:** one watches competitors ("what changed"), one watches customer
language across X + Reddit, one watches creators in the niche for formats worth
testing, one watches ads + landing pages.

**Hermes-style examples:** "every Monday build a market brief", "every Friday review
the experiments", "each fresh batch of sales calls → pull objections → update the
positioning file".

## Agents wired to live data — the SEO example

Beginner move: ask AI to "write a blog post about a keyword." Marketing-engineer move:
1. Check Google Search Console.
2. Pull keyword data from Ahrefs / SEM Rush.
3. Check the CMS for whether it already exists.
4. Rank opportunities by **buyer intent, product relevance, ranking distance, and search volume**.
5. Research what's already ranking.
6. Add the founder's POV.
7. Draft the post, write the meta title, suggest internal links.
8. Send the whole thing for approval.

The agent has a job, inputs from the business, an approval gate, and a place to write
back what worked.

## The six growth systems

Worked example throughout: a vertical SaaS selling to **commercial HVAC contractors**.
Sharp angle — "**Stop losing replacement revenue after every service call**" — beats
"run your HVAC business better."

### S1 — Customer truth system  → `market-truth.md`
Inputs: sales calls, support tickets, churn notes, Stripe movement, product analytics
(PostHog), CRM notes, Reddit/X, reviews. Job: show **what changed**. Updates daily or
weekly by signal volume. **Receipts, not summaries** — quote snippets, ticket links,
event counts. Bad: "customers want better collaboration." Good: "five sales calls this
week mentioned emergency dispatch, but the calls that converted all talked about
missed follow-up quotes after the tech left."

### S2 — Founder content engine  → `02-content-engine/`
Record the founder talking to customers; pull from podcasts; extract the strongest
ideas; have the system watch what performs (which hooks keep getting watched); make
more of what wins. **One insight → five assets:** founder post, short video, landing
page line, cold-email angle, calculator. "The system turns a real pain into distribution."

### S3 — Outbound signal engine  → `03-outbound-engine/`
Bad outbound starts with a spreadsheet of names. Good outbound starts with **timing**:
who just raised, who's hiring for the exact problem you solve, who posted about the
pain, who fits ICP and has a reason to care this week. Agent watches signals →
researches accounts → drafts specific angles → human approval. Painkillers, not vitamins.

### S4 — Creative testing engine  → `04-creative-testing/`
One offer → 20 hooks, 10 ad angles → record results → test. "'Facebook ads don't work
for me' — maybe you're just not testing enough creative with the right angle."
Creative as a learning system, not a treadmill. Can generate thousands of variants off
the positioning.

### S5 — AI search visibility
A billion+ people ask ChatGPT (plus Google AI overviews, Gemini, Perplexity, Claude).
Is the company understandable to those systems? Have agents pull that data, create
content, optimise the site to **be the cited source**. Getting cited by AI is a large
open opportunity.

### S6 — Growth cockpit + agent evals
**Cockpit** (`growth-cockpit.md`): weekly view — what content worked, what campaign
created real conversations, which objection recurred, what test won, what % of tests
won, what competitors moved, what pain is getting louder, what to test next. HVAC
example: "lost replacement revenue angle drove fewer clicks than the dispatch angle,
but twice as many demo requests from owners with 20+ techs."
**Evals** (`05-agents/_evals-checklist.md`): every agent output checked for founder
voice · customer words · cites receipts · right buyer · gets approval · creates pipeline.

## The 30-day plan

- **Week 1 — Audit one company.** Study website, offer, ICP, founder content, sales
  calls + support tickets. Output a **market map**: who's the customer, what pain do
  they describe, what words do they use, what are they buying instead, where's the
  funnel leak, what would you test first.
- **Week 2 — Build the growth repo.** Create it, add the folders, produce the first
  `market-truth.md`. Tools matter less than the workflow.
- **Week 3 — Your first machine.** Build ONE system (content engine / outbound signal
  engine / landing-page tester). One working system beats five half-built ones.
- **Week 4 — Results.** Did replies improve? Meetings booked? Conversion lift? Founder
  sound sharper? End with a case study: "audited the growth, built the customer-truth
  repo, found one high-intent pain they didn't know about, turned it into an outbound
  signal engine — shipped 75 targeted messages, 9 warm replies, 3 booked calls,
  documented everything."

## Monetisation (four paths)

1. **In-house** — become the person building the growth system ($250K–$500K, sits next to revenue).
2. **Consulting** — embed 30/60/90 days, install one system, sell the outcome ($5K–$30K/mo).
3. **Productised service** — one wedge, one market (e.g. "outbound signal engines for
   vertical SaaS", "founder content engine for B2B CEOs", "customer-truth repos for
   seed-stage startups"). Tighter wedge = easier to sell, deliver, repeat.
4. **Software** — turn the repeated pain into SaaS. Do it last: build by hand for
   5–10 companies first, notice what repeats, then productise. Avoids building what nobody wants.

Order: consult → spot the repeated system → productise → software.

## Caveats

- "The tools change. The workflow is the skill." Build around the workflow, never a product.
- "The agents are going to be a commodity. Your judgment about what to point them at is the moat."
- AI outbound needs a **banned-language** list or it gets weird fast.
- Customer-truth output must carry **receipts**, never a vague summary.
- Agent success metric = **qualified replies / pipeline**, never activity counts.
- Every agent job spec ends with **write results back**; every correction becomes a repo rule.
- Build ONE system fully before starting a second.
