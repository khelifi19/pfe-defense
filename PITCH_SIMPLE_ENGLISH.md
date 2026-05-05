# 🎤 Complete Pitch — Simple English Version v11 FINAL

**Yassine Khelifi · M2 SIA · CA-GIP · 15 minutes · 16 slides**

> Read out loud. Time yourself. Aim for 14:45.
> **Bold** = stress. *Italics* = pause briefly. `[ACTION]` = stage direction.

---

## 🎬 SLIDE 1 — Cold Open (1:30)

`[Open in fullscreen. Stand still. Don't speak for 3 seconds. Let the counter tick to 88,343.]`

> Good afternoon.
>
> *Tuesday morning. 9:47 AM. Paris.*
>
> Somewhere in the city, a customer opens her LCL banking app. She wants to send money. **It's urgent.** She sees a spinning wheel.
>
> Two hundred meters away, in a Crédit Agricole data center, **one thousand alerts have just lit up.** And in the last three months — **eighty-eight thousand alerts.**
>
> *And nobody knows which one is hers.*
>
> `[Pause 2 seconds]`
>
> My name is Yassine Khelifi. For the next fifteen minutes, I will tell you how I helped to answer that question.

---

## 🪪 SLIDE 2 — Title (0:30)

`[Click → next slide. Gesture briefly to the two university logos at the bottom]`

> This project is called **Predictive AIOps — the Weak Signal Cockpit.** I built it during my final-year internship at CA-GIP, in Paris.
>
> I am a double-degree student between **ESPRIT in Tunis** and **Université Gustave Eiffel** here in France.

---

## 📋 SLIDE 3 — Table of Contents (0:20)

`[Click → next slide]`

> Here is what we will see together. **Eight chapters.** One customer. One cockpit. One engineer.

---

## 🔬 SLIDE 4 — Problématique (0:40) 🆕 NEW

`[Click → next slide. Read the question slowly, with weight. Pause before each "Data Science" / "infrastructure" / "regulated"]`

> Before I tell you the story, let me share **the research question** behind this entire project.
>
> `[Pause 2 seconds]`
>
> *How can a* **Data Science** *approach solve complex* **infrastructure monitoring** *problems in a* **regulated banking environment** *?*
>
> `[Pause 2 seconds. Gesture to the 3 pillars at the bottom]`
>
> Three pillars. **Data Science** — a local AI model. **Infrastructure** — 88,343 alerts across 90 days. **Regulated** — *zero data ever leaves the bank.*
>
> Everything I will show you in the next thirteen minutes — is my answer to this question.

---

## 🌍 SLIDE 5 — The Stage (1:30)

`[Click → next slide. Click each card while talking about it]`

> To understand my project, you need to understand four things.
>
> `[Click the Crédit Agricole card]` **First — Crédit Agricole.** A French bank, founded in 1894. Today the **ninth largest bank in the world.** Fifty-four million customers.
>
> `[Click the CA-GIP card]` **Second — CA-GIP.** This is **the engine room.** It runs the cloud and the monitoring for the whole Group. **Eighty percent** of the Group's IT runs through CA-GIP.
>
> `[Click the LCL card]` **Third — LCL.** Le Crédit Lyonnais. **The bank I monitored.** Its applications generated the eighty-eight thousand alerts I studied.
>
> `[Click the COD card]` **Finally — the COD, the Centre of DevOps.** This is where I worked. Four squads inside. **I worked in two of them** during my six months.

---

## 🛤️ SLIDE 6 — Journey + Agile (1:50)

`[Click → next slide]`

> So my six months had two phases.
>
> **Phase one — Squad Tools. November to January.**
>
> Day one, I get a Jira ticket: DEV-895. *"Build a page where users can upload a file."* I built it in React. After thirty days, it was live in production.
>
> *But while watching how people used my page, I noticed something strange…*
>
> **Phase two — Squad DevOps. February to May.**
>
> I opened a tool called Dynatrace for the first time. **One thousand alerts on my screen.** Strange codes. And the data only goes back thirty days. After that, it disappears.
>
> *This is not a tool problem. It is a management blindness problem.*
>
> `[Gesture to the Agile banner]`
>
> One more thing. Both phases happened inside CA-GIP's **Agile and Scrum framework.** Sprints. Daily stand-ups. Sprint reviews. Every three months, **PI Planning** with fifty engineers in one room.
>
> These rituals are **not bureaucracy.** They are how a real engineering team stays together.

---

## 💬 SLIDE 7 — The Problem · Dialogue (1:00)

`[Click → next slide. Read with two voices]`

> Let me show you the moment I saw the problem.
>
> `[Voice 1 — manager, calm]` **Manager:** *"Yassine, how many incidents did we have on the API Gateway last month?"*
>
> `[Voice 2 — me, hesitating]` **Me:** *"Uh... Dynatrace only keeps thirty days."*
>
> `[Voice 1]` **Manager:** *"And the month before?"*
>
> `[Voice 2 — quietly]` **Me:** *"…lost."*
>
> `[Pause 3 seconds. Look at the jury.]`
>
> That is where the project began.

---

## 🍽️ SLIDE 8 — Pipeline + ROI (2:00)

`[Click → next slide]`

> So I designed a solution. **Think of my project as a restaurant.**
>
> **Station one — the market.** The Dynatrace API. The raw alerts.
>
> **Station two — the sous-chef.** A Python script. It cleans and translates the alerts.
>
> **Station three — the head chef.** **Mistral**, an open-source AI running on a local server inside the bank. It scores each alert from 1 to 10. **The chef stays in the kitchen.** No data ever leaves.
>
> **Station four — the cold room.** JFrog Artifactory. Every result, dated and versioned.
>
> **Station five — the plate.** Power BI. Seven pages of clarity.
>
> `[Gesture to the ROI banner]`
>
> The important part — this whole pipeline cost the bank **zero euros.** Open-source AI. Tools already licensed. **No new license. No new server.**
>
> *Same data. Different presentation. **That is the entire project.***

---

## 🔍 SLIDE 9 — The Finding (1:20)

`[Click → next slide]`

> Once the pipeline was running, **the data started speaking back.**
>
> When you put 90 days of alerts side by side, a pattern appears.
>
> `[Point to the orange bar]`
>
> **Every Tuesday morning. The same hour. The same spike.**
>
> `[Pause 2 seconds]`
>
> A weekly batch job, every Tuesday at 9:30. **Invisible at thirty days. Unmistakable at ninety.**

---

## ⚖️ SLIDE 10 — Before / After (1:00)

`[Click → next slide. Don't speak for 3 seconds.]`

> Side by side.
>
> **On the left** — what managers used to see. Cryptic codes. Thirty days of memory. Built for engineers — not for them.
>
> **On the right** — what they see now. Ninety days. Business labels. AI risk scores. The Tuesday peak — visible for the first time.
>
> Same Dynatrace. **Different lens.**

---

## 📊 SLIDE 11 — The Cockpit (1:50)

`[Click → next slide. Click through the tabs]`

> Here is the result. Live.
>
> `[Click tab 1]` Page one — the global view.
>
> `[Click tab 2]` Page two — the trend over time.
>
> `[Click tab 3]` Page three — the technical root causes.
>
> `[Click tab 4]` Page four — the Tuesday peak again.
>
> `[Click tabs 5 and 6 quickly]`
>
> The other pages handle drill-down per incident, AI risk scores, and a one-line explanation written by Mistral.
>
> Seven pages. **Same data, every audience.**

---

## 🚀 SLIDE 12 — Roadmap (1:15)

`[Click → next slide]`

> Now, version one is just the beginning. Here is the roadmap.
>
> `[v1 card]` **Version 1** — what I delivered. The rules-based cockpit. Running today.
>
> `[v2 card]` **Version 2** — the next six months. Replace my hand-written rules with **DBSCAN**, a machine-learning model. *No human maintenance.* It will read directly from **Kubernetes** logs.
>
> *You may wonder — why do we jump from v2 to v4?*
>
> `[Gesture to "Why skip v3" banner]`
>
> **Version 3 is internal tuning** — performance fixes for the engineers. *Invisible to managers.*
>
> `[v4 card]` **Version 4 — the long-term vision.** Replace the nightly batch with a **Kafka real-time pipeline** running on Kubernetes. From hours to **seconds.**

---

## 🎯 SLIDE 13 — Skills Acquired (1:00)

`[Click → next slide]`

> Three dimensions of growth.
>
> **Technical.** Python, the Mistral local AI, Power BI, and very importantly — **Kubernetes.** I learned to read namespaces, query logs with kubectl. *I am preparing the official CKA certification.*
>
> **Methodology.** Twelve sprints. PI Planning. DevOps culture. Architecture that survives in production.
>
> **Human.** Talking to LCL stakeholders and DevOps engineers in the same week. Translating tech into business. Finding problems on my own.
>
> *A Data Scientist who does not understand infrastructure is a doctor who does not know where the hospitals are.*

---

## 🔄 SLIDE 14 — Callback (0:30)

`[Click → next slide]`

> Remember the customer from the very beginning? Tuesday, 9:47 AM.
>
> `[Pause 2 seconds]`
>
> Today, her transfer still fails sometimes.
>
> But tomorrow — **the manager knows.** And at the next incident, she will wait **five seconds** instead of **five minutes.**
>
> *That is what this internship was about.*

---

## 🎯 SLIDE 15 — Closing (0:25)

`[Click → next slide. Pause 3 seconds. Speak slowly.]`

> So, to close.
>
> **I arrived a Data Scientist. I leave an engineer.**
>
> CKA in progress. MLOps as the next chapter. Building AI systems that survive in production.
>
> Thank you for your attention.

---

## ❓ SLIDE 16 — Q&A

`[Smile. Stand still. Wait.]`

> I would be very happy to take your questions.

---

# ⏱️ Updated timing — 16 slides

| # | Slide | Time |
|---|---|---|
| 1 | Cold Open | 1:30 |
| 2 | Title | 0:30 |
| 3 | TOC | 0:20 |
| 4 | **Problématique 🆕** | **0:40** |
| 5 | Stage | 1:30 |
| 6 | Journey + Agile | 1:50 |
| 7 | Problem | 1:00 |
| 8 | Pipeline + ROI | 2:00 |
| 9 | Finding | 1:20 |
| 10 | Before/After | 1:00 |
| 11 | Cockpit | 1:50 |
| 12 | Roadmap | 1:15 |
| 13 | Skills | 1:00 |
| 14 | Callback | 0:30 |
| 15 | Closing | 0:25 |
| | **TOTAL** | **15:00** |

---

# 🎯 The 4 jury hooks

1. **Slide 4 — Problématique.** State the research question with weight. *"Data Science · Infrastructure · Regulated."* This is your academic anchor.

2. **Slide 6 — Agile rituals.** Shows professional maturity.

3. **Slide 8 — Zero-cost ROI.** Business value.

4. **Slide 12 — Roadmap.** Forward-thinking vision.

If the jury only remembers four things, those are the four.

---

# 🆘 If you blank out

Say *"Let me move to the next chapter,"* and click forward. The slides will pull you back in. The visual is your safety net.

Bonne soutenance Yassine. 🎯
