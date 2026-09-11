# Features and specification

## Context
Student teams need to define completion, expose gaps, and assign repairs. Early finishers inherit editing while constrained contributors miss unstated standards. The system supports handoffs so teams finish a combined draft 48 hours early and rehearse.

## Users
The primary users are the **early-finishing integrator** and **time-constrained section owner** in [USERS.md](USERS.md): one needs visibility; the other, clear expectations and early correction.

## Scope
The system records deadlines, owned sections, checkable completion criteria, evidence, review outcomes, accepted repair assignments, and rehearsal completion.

It does **not** create slides, judge evidence quality, grade or rank members, schedule meetings, send external messages, or reassign work automatically.

### Kano hypotheses
 These are tentative hypotheses, not validated survey findings.

| Feature ID | Feature | Kano hypothesis | Segment / date | Evidence and reasoning |
|---|---|---|---|---|
| F-01 |Definition-of-done checklist | Must-be|Both / 2026-09-10 |Both interviews linked repairs to unclear standards. |
| F-02 |Owner and review status |Must-be |Integrator / 2026-09-10 | Maya needed visible responsibility and readiness.|
| F-03 | Early peer review|Performance | Both / 2026-09-10 |Daniel needed feedback; Maya needed risk visibility.| 
| F-04 |  Automatic risk flag| Attractive|Integrator / 2026-09-10|It reduces Maya’s manual monitoring.| 
| F-05 |Themes and animations|Indifferent  | Both / 2026-09-10|Neither linked decoration to the job.|
| F-06 |Completion-speed ranking |Reverse|Constrained owner / 2026-09-10| Ranking punishes constrained schedules and invites judgment.|

## Behavior
1. A member creates a project with final and internal-draft times; the latter must be at least 48 hours earlier.
2. Each section requires different owner and reviewer members plus checkable completion criteria.
3. An owner attaches source links and requests review. The system records the time and changes **In progress** to **Review requested**.
4. The reviewer marks each criterion **Met** or **Not met** and explains unmet criteria. All met produces **Ready**; otherwise, **Revision needed**.
5. Twenty-four hours before the internal deadline, the system flags sections not **Ready**, showing owners and unmet criteria without reassignment.
6. A member may propose a repair owner and due time. Ownership changes only after that person accepts.
7. Only projects with all sections **Ready** may become **Combined draft ready**. A member may then record rehearsal.
8. Statuses, reviews, and ownership changes remain in a chronological activity record.

## Constraints

- The first version shall be a responsive web application.
- Project access shall be limited to invited members.
- It shall not require student identification numbers or grades.
- All displayed deadlines shall include the project’s selected time zone.
- Saved status changes shall appear within two seconds under normal network conditions.
- Members shall not edit activity records.


## Acceptance

- **F-01 — Event-driven:** When a member creates a section, the system shall require at least one checkable completion criterion.
- **F-01 — State-driven:** While any criterion is marked **Not met**, the system shall display **Revision needed** and the reviewer’s correction note.
- **F-02 — Ubiquitous:** The system shall display one owner, a different reviewer, and the current review status for every section.
- **F-03 — Event-driven:** When an owner requests review, the system shall record the request time and display **Review requested** within two seconds.
- **F-04 — Event-driven:** When 24 hours remain before the internal-draft deadline, the system shall flag every section not marked **Ready** and identify its unmet criteria.
- **Project readiness — State-driven:** While any section is not **Ready**, the system shall prevent the project from being marked **Combined draft ready**.
- **Repair ownership — Unwanted:** If a proposed repair owner declines, then the system shall preserve the existing owner and record the decline.
## Handoff reflection
A classmate reviewed this specification and identified “normal network conditions” as ambiguous because it does not define connection speed or system load. I revised the constraint to require saved status changes to appear within two seconds on a stable broadband or cellular connection. The remaining decisions are which authentication method to use and whether the system should validate only the format of source links or also confirm that each link is accessible.

## AI assistance
I used ChatGPT to understand the assignment requirements and create a step-by-step plan to follow. I also used it to organize my writing, format the required sections, and check the EARS notation. I reviewed and revised the final work to ensure it followed the assignment template and reflected my decisions.
