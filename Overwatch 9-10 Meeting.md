# Overwatch — Sprint Planning Meeting Notes

**Team:** Overwatch (CSC 131 Section 08)  
**Date:** Thursday, September 10, 2026  
**Type:** Internal team sprint planning (after client lecture)  
**Attendees (from call):** Josh (PM), Mohd (Infra/Tech Lead), Connor (Frontend Engineer), Parker (Frontend UI/UX), Ali (Backend/Integration), Ryan (Backend Logic)

---

## 1) Purpose

Align on Sprint 1 priorities after the Laura Gonzalez client lecture and assign concrete near-term work.

---

## 2) Shared understanding of client priority

Laura’s biggest issue: **no reliable data** on campus dumpster pickups.

**Priority #1 for Overwatch:**
1. Help get that data collected
2. Make it easy for her to understand

**Not Sprint 1 focus:**
- AI contamination / second project idea = stretch only if core path is crushed later

---

## 3) Sprint 1 goal (Sep 10 → demo Sep 24)

Josh proposed two tangible outcomes:
1. Contribution toward a **shared survey** being ready
2. A **working dashboard prototype** showing how information will be displayed

Team agreed this is a reasonable Sprint 1 workload (not overloaded).

---

## 4) Key decision: sequencing

### Unclear still
- Whether class uses **one shared survey** vs each team making its own
- Laura’s other-campus **survey template** not available yet
- Professor reply to Josh on survey ownership was incomplete (recording question answered vaguely; survey question not answered)

### Decision made in meeting
- **Do not build survey layout/UI yet**
- **Hyper-focus first on dashboard prototype**
- Meanwhile:
  - **Mohd** drafts survey **questions** Josh can send Laura
  - As dashboard work reveals more needed fields, add questions and escalate through Josh/Mohd
- Once Laura/professor clarify shared Smartsheet/template vs custom survey, resume survey implementation work

Rationale discussed:
- Drivers filling 8 team surveys would be bad
- Campus already has Smartsheet membership / likely economical default unless a team invents something clearly better
- Dashboard work can proceed with mock data now
- Waiting on live survey responses should not block development

---

## 5) Role assignments for Sprint 1

### Josh (Project Manager)
- Client + professor communication
- Follow up on survey shared-vs-own / template clarity
- Email Laura (and professor as needed)
- Forward answers to team
- Coordinate survey questions (including with other teams if required)
- Deliverable #1 submission logistics

### Mohd (Infrastructure / Tech Lead)
- Draft survey questions for Josh to send
- Lead technical setup thinking for accessing/connecting survey data later
- Bridge frontend + backend (effectively supporting both sides)
- When backend sample data is ready, transfer it into frontend correctly with no loss

### Connor + Parker (Frontend)
- Focus on **dashboard prototype**
  - layout / look-and-feel / UX simplicity
  - early frontend engineering as needed
- Parker exploring **Penpot** (said “pen pie”) / design tooling; can ask team for help
- Survey layout paused for now
- Placeholder dashboard content ideas mentioned:
  - stream mix pie/donut (landfill / compost / recycle)
  - fullness-by-location style chart (e.g., Union likely higher)
- Visual direction idea floated: green/white (Sac State + sustainability); Parker to refine

### Ali + Ryan (Backend)
Confirmed first steps:
1. Draft **data model** / what a pickup event looks like  
   (dumpster ID, location, stream, fullness threshold logic, datetime, driver, photo ref, etc.)
2. Use existing bin names/codes structure (plug real campus list in when Laura sends it)
3. Create **sample/mock records** so frontend is not designing on an empty canvas
4. Optional later in sprint: script that summarizes survey/mock data and/or simple endpoints like `GET /pickups`, `GET /stats`

Ali also raised integration angle: once survey exists, help mesh frontend survey/dashboard with backend data flow.

### Important mindset (from Ryan Todd, repeated by Josh)
Design/program by asking: **what does Laura need most when she opens the dashboard?**  
Not random charts for their own sake.

---

## 6) Meetings cadence

- Regular Overwatch meetings: **Monday & Wednesday at 3:00 PM**
- Prefer in person
- If someone cannot attend in person (Ali specifically may often remote): join the call
- Early sprint planning sessions can run longer than normal standups

---

## 7) Deliverable #1 discussion

- Team name in doc should be **Overwatch** (replace leftover “Blueprint” references)
- Roles/experiences largely present
- SharePoint/Word collab not updating reliably for everyone → move to **Google Docs** for final edits
- Professor wants ~1–2 pages **double-spaced**
- Bios should be shortened (target discussed: ~3 sentences ideal, up to ~4–5 if needed)
- Josh will submit after revisions; asked for edits by his break (~8:30–9:00 PM)
- Josh sharing Google Doc + collecting personal Gmails as needed

---

## 8) Docs / GitHub process mentioned

- Maintain shared **context** document in org **context** repo
- Push **meeting notes** (this file) to org **meeting notes** repo
- Meeting notes as markdown
- Ensure GitHub org invites accepted (Josh needed to accept invite; usernames confirmed: chev2 = Connor, StudentP77 = Parker)
- Ali offered/confirmed maintaining context and pushing updates

---

## 9) Action items

| Owner | Action | Due / notes |
|---|---|---|
| All | Shorten Deliverable #1 bios/guidelines; finalize Google Doc | Before Josh submits tonight |
| Josh | Submit Deliverable #1 | Tonight by midnight |
| Josh | Email Laura + follow up professor on survey shared/template clarity | ASAP |
| Mohd | Draft baseline survey questions for Josh to send | ASAP |
| Connor + Parker | Start dashboard prototype (design + early FE) | Sprint 1 |
| Ali + Ryan | Draft pickup data model + mock/sample dataset | Sprint 1 immediate |
| Mohd | Integrate/transfer sample backend data into frontend when ready | After BE sample exists |
| All | Mon/Wed 3pm meetings | Ongoing |
| Ali (+ team) | Review then push context.md + these meeting notes to GitHub repos | After review |

---

## 10) Open questions leaving the meeting

1. One shared class survey vs team-specific survey?
2. When does Laura’s survey template / Smartsheet access arrive?
3. Exact Definition of Done for Sep 24 dashboard prototype (clickable UI only vs wired to mock API/CSV)?
4. Will Monday client feature-list expansion change Sprint 1 scope?

---

## 11) One-line summary

**Overwatch Sprint 1:** build a Laura-focused dashboard prototype with real-looking mock pickup data now; draft survey questions in parallel; pause survey UI until shared-survey/template questions are answered; meet Mon/Wed 3pm; finish Deliverable #1 tonight.
