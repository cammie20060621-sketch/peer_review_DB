# Peer Review Report

> **Instructions:** Complete this form **individually and independently**.
> Do not discuss your ratings with teammates before submitting.
> Submit via EEClass as a **separate, confidential submission** — not in the shared team repo.
> Your teammates will not see this report.
>
> Reference the team's `WORK_ALLOCATION_TEMPLATE.md` when completing this form.

---

## Your Details

| Field | Your answer |
|-------|------------|
| Full Name | 薛閔云 |
| Student ID | 113403528 |
| Team ID | 17 |
| Date submitted | 2026/06/12 |

---

## Rating Scale

| Rating | Meaning |
|--------|---------|
| **5** | Exceeded expectations — delivered more than agreed; helped teammates; consistently high quality |
| **4** | Met expectations fully — delivered exactly what was agreed; on time; good quality |
| **3** | Mostly met expectations — minor shortfalls; one or two items completed late or with help |
| **2** | Partially met expectations — noticeable gaps; teammates had to cover some tasks |
| **1** | Did not meet expectations — significant tasks left incomplete; very limited contribution |

---

## Section A — Self-Assessment

### A1. What did you personally implement?

List the specific tasks, functions, files, or document sections that you were the primary author of.
Be specific (e.g., "I designed all 12 tables in schema.sql and implemented query_national_rail_availability and execute_booking").

> *Your answer:*
>I mainly worked on the PostgreSQL relational database part of the project. I helped design and refine the relational schema in `databases/relational/schema.sql`, including tables for users, metro stations, national rail stations, schedules, schedule stops, bookings, payments, feedback, fare classes, and seat layouts.
>
>I also worked on `skeleton/seed_postgres.py` to map the mock JSON data into the relational tables and debugged seeding issues caused by foreign key constraints, check constraints, and mismatched field names between the JSON files and the schema.
>
>In addition, I implemented and tested several relational query functions in `databases/relational/queries.py`, including user profile lookup, user bookings, fare calculation, seat availability, booking-related queries, and payment lookup. I also helped test the Gradio UI with the database debug panel and fixed an integration issue in `skeleton/agent.py` where the logged-in user profile used `name` instead of `full_name`.

---

### A2. What challenges did you face?

Describe any technical or collaboration difficulties you personally encountered and how you resolved them.

> *Your answer:*
>One major challenge was making the mock JSON data fit the relational schema correctly. Some JSON fields used different names from our schema, such as `first_train_time`, `last_train_time`, and `per_stop_rate_usd`, so I had to carefully map them to the correct database columns.
>Another challenge was debugging runtime issues after seeding. For example, I found that the UI sometimes gave an incorrect LLM summary even when the raw database result was correct. I resolved this by checking the database debug panel and comparing the tool result with the final chatbot response. I also encountered a login bug caused by a mismatch between `full_name` and `name`, which was fixed in `agent.py`.

---

### A3. Self-rating

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| I delivered the tasks assigned to me in the work allocation | 5 | I completed the relational database tasks I was responsible for, including schema refinement, PostgreSQL seeding, query implementation, and debugging. |
| The quality of my work was satisfactory | 4 | My work was functional and tested with the seed scripts and UI debug panel, although some integration issues required later fixes. |
| I communicated well and kept the team informed | 4 | I updated teammates about database progress and discussed issues when schema or seed changes affected other parts of the project. |
| I met deadlines agreed within the team | 4 | I completed my main tasks before submission and pushed my updates through GitHub for review. |
| **Overall self-rating** | 4 | I contributed consistently to the database implementation and debugging, especially on the PostgreSQL side. |

---

### A4. Estimated contribution percentage

What percentage of the total team effort do you estimate you personally contributed?

> My estimated contribution: **__33__%**

---

## Section B — Peer Assessments

Complete one subsection per teammate. Add or remove subsections to match your team size.
If your team has 2 members, complete B1 only. If 3 members, complete B1 and B2.

---

### B1. Assessment of Teammate 1

| Field | Your answer |
|-------|------------|
| Teammate's full name | 松怡琳 |
| Teammate's student ID | 113403535 |

#### What did this teammate deliver?

List the tasks, functions, files, or document sections that this teammate was the primary author of,
based on what you observed during the project (compare against the work allocation).

> *Your answer:*This teammate mainly worked on database seeding and final testing. They helped ensure that the mock data could be loaded into the system correctly and participated in checking whether PostgreSQL, Neo4j, pgvector, Ollama, and the Gradio UI could run together. They also helped test the example queries from the README and verify results through the database debug panel.

#### Did their actual contribution match the agreed work allocation?

> *Your answer (Yes / Mostly / Partially / No — with explanation):*Yes. Their actual contribution matched the agreed work allocation because they completed the seeding and final testing tasks and helped confirm that the full system could run before submission.


#### Peer rating for this teammate

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| Delivered the tasks assigned in the work allocation | 4 | She completed the seeding and final testing tasks assigned to them. |
| Quality of their work was satisfactory | 3 | She work helped confirm that the databases and UI could run correctly together. |
| Communicated well and kept the team informed | 4 | She shared testing progress and helped identify issues during final system checks.|
| Met deadlines agreed within the team | 5 | They completed the testing-related work before submission and supported the final integration stage. |
| **Overall rating for this teammate** | 4 | They contributed reliably to seeding, testing, and final project verification. |

#### Estimated contribution percentage for this teammate

> My estimate of their contribution: **__33__%**

---

### B2. Assessment of Teammate 2

| Field | Your answer |
|-------|------------|
| Teammate's full name | 張藝齡 |
| Teammate's student ID | 113403013|

#### What did this teammate deliver?

> *Your answer:*This teammate mainly worked on the Neo4j graph database part of the project. They were responsible for designing the graph model, including `MetroStation` and `NationalRailStation` nodes, `METRO_LINK`, `RAIL_LINK`, and `INTERCHANGE_TO` relationships. They also worked on Neo4j seeding and route-related query functions.


#### Did their actual contribution match the agreed work allocation?

> *Your answer (Yes / Mostly / Partially / No — with explanation):*Yes. Their actual contribution matched the agreed work allocation because they completed the main Neo4j-related tasks and helped make the graph routing functions work with the TransitFlow UI.

#### Peer rating for this teammate

| Criterion | Rating (1–5) | Justification (1–2 sentences) |
|-----------|-------------|-------------------------------|
| Delivered the tasks assigned in the work allocation | 5 | She completed the main Neo4j graph database tasks, including graph structure and route query implementation. |
| Quality of their work was satisfactory | 4 | Her work supported the route-related UI tests, and the raw database results showed that the graph queries could return valid paths. |
| Communicated well and kept the team informed | 4 | She communicated progress and discussed route-related issues when team testing found problems. |
| Met deadlines agreed within the team | 4 | She completed their main tasks within the project timeline and helped with final integration. |
| **Overall rating for this teammate** | 4 | They made a solid contribution to the graph database part of the project and completed their assigned role. |

#### Estimated contribution percentage for this teammate

> My estimate of their contribution: **__33__%**

---

## Section C — Contribution Percentage Summary

All members (including yourself) must sum to 100%.

| Member | Your estimated % | Notes |
|--------|----------------|-------|
| Yourself | 34% | Mainly worked on PostgreSQL schema, seeding, queries |
| Teammate 1 | 33% | Mainly worked on Neo4j graph database and routing queries. |
| Teammate 2 | 33% |  Mainly worked on documentation, RAG/vector design, and final integration testing. |
| **Total** | **100%** | |

---

## Section D — Overall Team Reflection

### D1. What went well in the team's collaboration?

> *Your answer (2–4 sentences):*
>Our team was able to divide the project into different database components, including PostgreSQL, Neo4j, and RAG/vector search. We also used GitHub branches and pull requests to combine our work. When errors happened during seeding or UI testing, we discussed them and debugged them step by step.

---

### D2. What would you do differently if you did this project again?

> *Your answer (2–4 sentences):*
>If we did this project again, we would finalise the schema earlier before implementing seed scripts and query functions. Some issues happened because the mock data and schema did not fully match at first. We would also create a shared testing checklist earlier so that each member could verify their part more systematically.

---

### D3. Is there anything else the markers should know about team dynamics or individual contributions?

This is optional. Use it only if there is important context that the ratings above do not capture
(e.g., a member had a documented personal emergency, or a member was unresponsive for a significant period).

> *Your answer (or "Nothing to add"):*
>Nothing to add.

---

## Declaration

I confirm that this peer review reflects my honest and independent assessment.
I understand it will be kept confidential from my teammates.

**Signed:** ______薛閔云___________________________ **Date:** ____2026/06/12___________