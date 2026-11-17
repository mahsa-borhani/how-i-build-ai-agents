# How I build AI agent systems a business can trust

I built a team of AI agents myself, in Claude Code: about twenty roles across sales, operations, reporting, advertising
and QA. It works on a live commerce business every day, doing monitoring, reporting, anomaly alerts, forecasting and
research across the store, advertising, search and CRM. It had 22 versioned releases between April and October 2026.

This page is the method, in my own words. No company code, data or names are published here.

## The shape

- Each agent has one role and a written playbook.
- Work moves through a pipeline: drafted from live data, checked by a second agent, approved by a person.
- I wrote the architecture, the prompts, the review rules, the gates and the releases myself.

## Four rules, enforced in code rather than remembered

1. **The agent that produces never reviews.** A different agent checks the work.
2. **Outside claims need two independent sources.** Nothing customer-facing rests on one source.
3. **Anything irreversible waits for a person.** Spending, sending and deleting stay human decisions.
4. **Every change is versioned.** Releases live in Git, so any change can be traced and undone.

## Why the rules exist

In August I reviewed 32 incidents and found one cause behind them: the agent that did the work had also certified it.
I rebuilt the system around separation of duties.

## Proof that the brakes work

- QA sends back four in ten first drafts, and half of content drafts. A gate that never fails anything is decoration.
- An automated finding once proposed cancelling five container orders as duplicates. The human-approval rule held, and
  all five orders were real.

## Least privilege

The system gets the narrowest permission that works. Its Microsoft 365 access, for example, is an Entra ID app holding a
single `Sites.Selected` permission, which reaches nothing until an administrator grants it one named SharePoint site. I
send IT a ready-to-approve request with the options and troubleshooting notes spelled out, so security and speed come
together. That pattern has carried about fifteen Microsoft 365 requests so far.

## Forecasts are checked, not asserted

The forecasting agent resamples real orders, including the rare very large ones. It out-predicted the target three
30-day sprints running, and the fourth sprint's range was written down before any order existed. Targets now start from
the forecast.

## Teaching people to use it

The system comes with a plain-English guide, role playbooks and safety rules, an AI adoption plan for leadership and an
AI-assisted interview kit for hiring. I've coached six colleagues one-on-one on AI tools, from the business owner and the
controller to the supply chain manager and the sales lead. Adoption comes from people seeing their own task done faster.
I'm now coordinating the AI implementation across two companies in the group.

---

Business stories: [mahsaborhani.com](https://mahsaborhani.com) · [LinkedIn](https://www.linkedin.com/in/mahsa-borhani)
