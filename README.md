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

### Connect with me

<p align="left">
<a href="https://www.linkedin.com/in/bintang-basmara-5a347b371" target="_blank" rel="noreferrer" title="LinkedIn"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="LinkedIn" height="30" width="40"/></a>
<a href="https://www.instagram.com/bintang_basmara" target="_blank" rel="noreferrer" title="Instagram"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="Instagram" height="30" width="40"/></a>
</p>

---

### Languages and Tools

<p align="left">
<a href="#" title="JavaScript"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript" width="40" height="40"/></a>
<a href="#" title="Python"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" width="40" height="40"/></a>
<a href="#" title="PostgreSQL"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" alt="PostgreSQL" width="40" height="40"/></a>
<a href="#" title="Supabase"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/supabase/supabase-original.svg" alt="Supabase" width="40" height="40"/></a>
<a href="#" title="Flutter"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/flutter/flutter-original.svg" alt="Flutter" width="40" height="40"/></a>
<a href="#" title="Dart"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dart/dart-original.svg" alt="Dart" width="40" height="40"/></a>
<a href="#" title="HTML5"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" alt="HTML5" width="40" height="40"/></a>
<a href="#" title="CSS3"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" alt="CSS3" width="40" height="40"/></a>
<a href="#" title="Git"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" alt="Git" width="40" height="40"/></a>
</p>

Plus the parts with no logo to show: **n8n**, the **WhatsApp Cloud API**, the **Telegram Bot
API**, and **Google Apps Script** — which is where most of the actual work happens.

Open to automation and internal-tooling work.

---

<p align="center">
<img src="https://streak-stats.demolab.com/?user=basmarabintang-source&theme=dark&hide_border=true" alt="GitHub streak" />
</p>
