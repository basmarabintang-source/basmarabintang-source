### Hi, I'm Bintang

I work out what a business should automate, then build it — mostly in **n8n**, on top of
**Supabase / Postgres**, with WhatsApp and Telegram as the parts people actually touch.

Day to day that means running the internal systems for a motorcycle dealership: staff
attendance with face check and per-branch geofencing, a CRM that keeps the sales pipeline
honest, service reminders that reach the right customer on the right day, and a workshop
board on a TV so nobody has to walk over and ask where a bike is.

Most of that work is private. What is here is the part I can show.

---

### Public work

**[n8n-finance-workflows](https://github.com/basmarabintang-source/n8n-finance-workflows)** —
three finance pipelines built to be read, not just demoed:

| | what it decides |
|---|---|
| **AP 3-way match** | whether an invoice gets paid untouched, needs one named approver, or stops in a queue owned by the team that can fix it |
| **AR collections** | who gets chased today, who is left alone because they are disputed or inside a promise to pay, and who has run out of rope |
| **HR onboarding** | which tasks a new hire actually needs, who owes each one, and who will not be ready on day one |

They import and run on seeded demo data with **no credentials**, so you can execute them and
read the real output instead of taking my word for it. The Xero, Slack and Gmail nodes are
real nodes, switched off — not HTTP calls pretending to be integrations.

**[arzopa](https://github.com/basmarabintang-source/arzopa)** — speak a sentence or
photograph a receipt, get a transaction back. Tesseract + OpenCV + Whisper, running locally,
because the data is somebody's spending and it should not leave the machine.

---

### How I check my own work

A workflow that finishes green is not a workflow that works.

The AP matcher ran green for days while never drawing down the goods receipt. One delivery of
600 units was quietly backing 1,300 units of invoices, and an invoice re-billing goods that
had already been paid for was routed to procurement to *"fix the price"* — a remedy that ends
in paying twice. Nothing errored. Every node was green.

So I count the items leaving every node and re-derive each decision from the source rows
instead of trusting the summary. That is how the three-way match got a real draw-down, how AR
stopped dropping a disputed invoice out of its own log behind a check that could never fail,
and how the run reports stopped printing *"sent"* about messages nothing had sent.

If a number in a report describes an intention rather than an event, it is a bug. Most of the
defects worth finding look exactly like success.

---

### Tools

`n8n` · `Supabase / PostgreSQL` · `JavaScript` · `Python` · `Flutter` · `WhatsApp Cloud API` ·
`Telegram Bot API` · `Google Apps Script`

Open to automation and internal-tooling work.
