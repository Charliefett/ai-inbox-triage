> **Prototype.** This demo can make up facts in its draft replies (prices, policies, hours). Don't use it with real customers. A safer redesign is in progress.
AI Inbox Triage

Turn a pile of unsorted customer messages into categorized, prioritized items — each with a drafted reply — in seconds.

Built as a working demo of practical AI implementation for small businesses: take a real, time-consuming manual task and automate it end to end.

The problem

Small businesses get a steady stream of mixed messages — quote requests, complaints, general questions — and someone has to read each one, figure out what it is, decide what's urgent, and write a reply. It's repetitive, it's slow, and it's easy to let an angry customer or a hot lead sit too long.

What it does

Paste in a batch of incoming messages. The tool:

Classifies each one — quote request, complaint, question, or other
Flags urgency — time-sensitive or upset customers rise to the top
Drafts a reply for each message, specific to its content, for a person to review before sending
Summarizes the batch — how many of each type, how many urgent
How it works
A single self-contained HTML page — no build step, no backend to run for the demo
Sends the batch to an LLM with a structured prompt that returns typed JSON (category, urgency, summary, drafted reply) per message
Renders the results sorted by priority, with one-click copy on each reply
Degrades gracefully when the AI layer isn't available — the layout and sample data still load
Try it

Open index.html in a browser. Click Load example inbox to see it work on a realistic set of messages, or paste your own.

From demo to production

This is the demonstration version. A production deployment for a business would:

Run the AI on a server-side API key, so the business needs no AI subscription of its own
Enforce per-account usage limits to control cost
Wire directly into the business's real inbox (email, web form, chat) instead of copy-paste
Match the company's branding and tone, trained on their own past replies
Never store or expose credentials client-side
About

Built by Charlie Fett — I find where AI fits a business's actual workflow, then build the system around it. More at github.com/charliefett.

Note: the demo's live AI step runs on the viewer's own LLM access; the production version runs on the operator's API key so end users need nothing.
