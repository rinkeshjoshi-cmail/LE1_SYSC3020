---
theme:
  name: catppuccin-latte
---

SYSC 3020: Introduction to Software Engineering
===

### Jira Guide · Running Your Sprint in Jira

**Fall 2026**

**TA:** Rinkesh Joshi · rinkeshjoshi@cmail.carleton.ca

**For:** Assignment 2 (Sprint 2) and every sprint after it

**Companion to:** the Assignment 2 lab walkthrough slides

<!-- end_slide -->

Jira 1: How the Pieces Fit
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

```
Space  SYSC3020_A1_TA  (Scrum, team-managed)
│
├─ Epic   SYSC-1  A1-Requirements
│   ├─ Story  SYSC-5  SJC-001 Pellet scores points
│   ├─ Story  SYSC-6  SJC-002 Player dies on ghost
│   ├─ Task   SYSC-8  Task A — Code Map
│   │   ├─ Sub-task SYSC-13  board package
│   │   ├─ Sub-task SYSC-14  level package
│   │   ├─ Sub-task SYSC-15  npc + npc.ghost
│   │   └─ Sub-task SYSC-16  points + Core Events
│   ├─ Task   SYSC-9  Task B — SRS (B1–B6)
│   ├─ Task   SYSC-10 Task C — Defect review
│   └─ …  (more items, not all shown)
│
├─ Sprint "A1 Sprint 1 — Requirements"  (+ goal)
└─ Backlog  SYSC-7, SYSC-12  (not in a sprint yet)
```

<!-- column: 1 -->

- **Epic**: the assignment (one per sprint)
- **Story**: a requirement / user-facing behaviour
- **Task**: a unit of work (Task A, B, C…)
- **Sub-task** (Jira: "Subtask"): one person's share of a task
- **Sprint**: the time-box + goal
- **Backlog**: work not in a sprint yet

**Screenshot 1 →** next slide

<!-- reset_layout -->

> **Note:** `SYSC-1`, `SYSC-5`, `SYSC-8`, … are just Jira **work item keys**: the demo space's key (`SYSC`) plus a number. They are **not** course codes. Your team's items use **your** space's key (e.g., `ABC-1`).
> Screenshots come from our demo space **SYSC3020_A1_TA** (A1, Sprint 1). *Reference only: one person made it in one sitting, so its history and times don't look like a real team's sprint.*

<!-- end_slide -->

Jira 1: How the Pieces Fit (Screenshot 1)
===

![image:width:100%](images/jira/01_hie.png)

<!-- end_slide -->

Jira 2: Backlog + Sprint Planning
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Step 1: Fill the backlog
Sidebar → **Backlog** → **+ Create** → work type
(Story / Task) → title → Enter.

### Step 2: Create the sprint
At the top of the backlog → **Create sprint**.

### Step 3: Plan it
**Drag** the work items you commit to from the backlog
into the sprint. Leave the rest in the backlog.

### Step 4: Start it
**Start sprint** → set:
- **Sprint name** (e.g., "A2 Sprint 2 — Design")
- **Duration** / **Start date** / **End date**
- **Sprint goal**: one line (graded!)

The **Board** only shows the items of a **started** sprint.

<!-- column: 1 -->

**Screenshots 2 and 3 →** next 2 slides

### Story or Task?

- **Story**: a requirement from the **user's** point of view
  (e.g., SJC-001 *Pellet scores points*)
- **Task**: work the team must **do**
  (e.g., *Draw SD-01*, *Consistency check*)
- Most A2 work (diagrams, checks) → **Tasks**

**Docs:**
https://www.atlassian.com/agile/tutorials/sprints

<!-- reset_layout -->

**Story vs Task (official):** https://www.atlassian.com/software/jira/guides/issues/overview

<!-- end_slide -->

Jira 2: Backlog + Sprint Planning (Screenshot 2)
===

![image:width:100%](images/jira/02_bklog.png)

<!-- end_slide -->

Jira 2: Backlog + Sprint Planning (Screenshot 3)
===

![image:width:100%](images/jira/03_edit_sprint.png)

<!-- end_slide -->

Jira 2: Changes After the Sprint Starts
===

### The usual order

1. Fill the **backlog** with stories + tasks (under the epic)
2. **Create sprint** → drag in the items you commit to
3. **Start sprint** (name, dates, one-line goal)

<!-- pause -->

### Need something new mid-sprint? You can add it.

- Create the work item → on the **Backlog**, **drag it into the active sprint**, or set its **Sprint** field
- Shared task? Add **sub-tasks** any time; they stay in their parent's sprint
- Editing items (description, assignee, status) is always allowed

<!-- pause -->

### But keep it rare

Work added after the start shows up as a **scope change** (the burndown line jumps up),
and so does changing an estimate after the start. Plan most of the work on **day 1**.

**Docs:** https://www.atlassian.com/agile/tutorials/burndown-charts

<!-- end_slide -->

Jira 3: Epics and Child Items
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### A **new** epic for every assignment (same space)

- A1 → "A1-Requirements" (our demo)
- A2 → **"A2 — Design: Structure & Interaction"**

### Create the epic (team-managed)
**Create** → work type **Epic** → name → **Create**.
(Or the **Timeline** tab, if enabled via **+** next to the tabs → **+** in the first column.)

### Put work under it
- Open any work item → set its **Parent** field to the epic, or
- On the **Timeline** (if enabled): hover the epic → **+ Create work item**.

Every story and task of the assignment should sit **under its epic**.

<!-- column: 1 -->

**Screenshot 4 →** next slide

**Docs:**
https://www.atlassian.com/agile/tutorials/epics

<!-- reset_layout -->

<!-- end_slide -->

Jira 3: Epics and Child Items (Screenshot 4)
===

![image:width:100%](images/jira/04_epic_child.png)

<!-- end_slide -->

Jira 4: Sub-tasks, One Person Each
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### A work item has **one** assignee

Jira has no "multiple assignees" field.

**Two people on one task?** You **can** break it into
**sub-tasks**, each with its **own assignee**.

### How
Open the task → create a **sub-task** from it (the **•••** menu,
or the add button under the title) → title → Enter → set its **Assignee**.

### Example (SYSC-8, Task A — Code Map)

| Sub-task | Who | Status |
|---|---|---|
| SYSC-13 board package | member-A | Done |
| SYSC-14 level package | member-B | Done |
| SYSC-15 npc + npc.ghost | member-C | In Progress |
| SYSC-16 points + Core Events | member-B | To Do |

<!-- column: 1 -->

**Screenshot 5 →** next slide: SYSC-8 (Task A) split into
**4 sub-tasks**, one per package, one assignee each.
Use it as a **reference**.

**Docs:**
https://support.atlassian.com/jira-software-cloud/docs/create-a-work-item-and-a-subtask

<!-- reset_layout -->

> Our demo has one account, so all items are assigned to one person and `member-A/B/C` labels stand in for teammates. **Your team assigns real people.**

<!-- end_slide -->

Jira 4: Sub-tasks, One Person Each (Screenshot 5)
===

![image:width:100%](images/jira/05_screenshot.png)

<!-- end_slide -->

Jira 5: Labels for Roles
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Make the roles visible

Add one **role label** to each work item, matching the
role the assignee plays **this sprint**:

`role-ProductOwner` · `role-ScrumMaster` · `role-QALead`

e.g., B is Scrum Master this sprint → items **assigned to B**
get `role-ScrumMaster`. Using sub-tasks? Each one gets
**its own assignee's** role.

Open the item → **Labels** field → type → Enter.
(No spaces in a label; use `-`.)

### Rotate every sprint (no repeats)

| Member | Sprint 1 (A1) | Sprint 2 (A2) |
|---|---|---|
| A | Product Owner | Scrum Master |
| B | Scrum Master | QA Lead |
| C | QA Lead | Product Owner |

### Filter by label
Board / backlog → **Filter** → **Labels** → tick a label
(e.g., `role-scrummaster`).

<!-- column: 1 -->

**Screenshots 6 and 7 →** next 2 slides

**Docs:**
https://support.atlassian.com/jira/kb/how-to-create-and-use-labels-in-jira-cloud
https://support.atlassian.com/jira-software-cloud/docs/show-or-hide-issues-on-your-board

<!-- reset_layout -->

<!-- end_slide -->

Jira 5: Labels for Roles (Screenshot 6)
===

![image:width:100%](images/jira/06_sysc11.png)

<!-- end_slide -->

Jira 5: Labels for Roles (Screenshot 7)
===

![image:width:100%](images/jira/07_filter.png)

<!-- end_slide -->

Jira 6: The Board (Move Cards As You Work)
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Columns = statuses

**To Do → In Progress → Done**

- Start a task → drag its card to **In Progress**
- Finish it → drag to **Done**
- **Do it on the day it happens**: every move is recorded with your name and the time

### What a healthy board looks like mid-sprint

Some cards in each column, sub-tasks finishing before
their parent, owners spread across the team.

### What loses marks

- Everything moved to **Done** in the last hour
- All cards created **after** the work was done
- One person moving every card

<!-- column: 1 -->

**Screenshot 8 →** next slide

Use the board **Filter** (**Assignee**, **Labels**, **Parent** = epic) to check
who is carrying what.

<!-- reset_layout -->

<!-- end_slide -->

Jira 6: The Board (Move Cards As You Work) (Screenshot 8)
===

![image:width:100%](images/jira/08_board.png)

<!-- end_slide -->

Jira 7: Stand-ups as Comments
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### What it is

A **short team meeting** (~15 min), **≥ 2× per week**.
What gets graded is the **record**: **every member's** three lines
(done / doing / blocked) as **comments in Jira**.

### How (every member, every stand-up)

1. Open a work item **you** are working on
2. **Activity** → add a comment (type `@` to mention a teammate)
3. Post it **from your own account**, on the day of the stand-up

**Each student posts their own.** Jira shows **who** posted each
comment, so one comment for the whole team can't show that the others took part.

<!-- column: 1 -->

**Screenshot 9 →** next slide

A **real** blocker + who is helping is better than
"Blocked: none" every time.

**Read:** https://www.atlassian.com/agile/scrum/standups

<!-- reset_layout -->

### Template (each member, each stand-up)

```
Stand-up — Thu Oct 15 · <name> (<role>)
Done:    finished SD-01 (pellet flow) in PlantUML
Doing:   class diagram associations for level package
Blocked: Graphviz missing on my laptop → asked <name>
```

<!-- end_slide -->

Jira 7: Stand-ups as Comments (Screenshot 9)
===

![image:width:100%](images/jira/09_subtask.png)

<!-- end_slide -->

Jira 8: Review, Retro, Complete the Sprint
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Last day: two short team meetings

1. **Sprint review**: demo the deliverable to each other
   (nothing to submit)
2. **Retrospective**: the team agrees on **3 bullets**
   (**Keep** · **Change** · **Try**): one set for the **team**,
   not per member

The retro bullets go in the **Team & Process** section of the design
page, so they end up in **design.pdf** (a Jira task like
SYSC-11, see **Screenshot 10**, is optional).

Write down **next sprint's roles** (rotation!).

### Then complete the sprint

Board → **Complete sprint** → choose where unfinished
items go (**backlog** or a **new sprint**).
The **Create a retrospective** (Confluence) box is optional;
your retro goes in the design page anyway.

A completed sprint stays in the history and reports:
**don't delete it or its work items.**

<!-- column: 1 -->

**Screenshots 10 and 11 →** next 2 slides

**Read:** https://www.atlassian.com/agile/scrum/retrospectives

<!-- reset_layout -->

<!-- end_slide -->

Jira 8: Review, Retro, Complete the Sprint (Screenshot 10)
===

![image:width:100%](images/jira/10_retro.png)

<!-- end_slide -->

Jira 8: Review, Retro, Complete the Sprint (Screenshot 11)
===

![image:width:100%](images/jira/11_dialog.png)

<!-- end_slide -->

Jira 9: History (What the TA Sees)
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Every change is logged, by person, with a timestamp

Open any work item → **Activity** → **History**.

History of our demo item **SYSC-5** (from Jira):

- Story point estimate → 3
  - *by Rinkesh Joshi, Oct 7, 02:23*
- Sprint → A1 Sprint 1 — Requirements
  - *by Rinkesh Joshi, Oct 7, 02:23*
- Status To Do → **Done**
  - *by Rinkesh Joshi, Oct 7, 02:23*

Comments (stand-ups) carry author + time too.

### So

- **Each member uses their own account**
- Move cards and post stand-ups **when it happens**
- Never delete and re-create items to "clean up"

<!-- column: 1 -->

**Screenshot 12 →** next slide

**Reports** (if enabled): **Burnup**, **Sprint burndown**,
**Velocity**, **Cumulative flow** (turn on: Space settings → Features).
https://support.atlassian.com/jira-software-cloud/docs/enable-reports

**Docs:**
https://support.atlassian.com/jira-software-cloud/docs/what-are-the-different-types-of-activity-on-an-issue/

<!-- reset_layout -->

<!-- end_slide -->

Jira 9: History (What the TA Sees) (Screenshot 12)
===

![image:width:100%](images/jira/12_activity.png)

<!-- end_slide -->

Jira 10: Sharing the Board With the TAs
===

### Before the deadline

1. **The student who created the site invites all the TAs**, the same way you invited teammates in A1
   (**•••** next to the space name → **Add people**, or Atlassian Administration → **Directory**
   → **Users** → **Invite users**) → each TA's Carleton email:
   - rinkeshjoshi@cmail.carleton.ca
   - HongboPang@cmail.carleton.ca
   - GhinwaYassin@cmail.carleton.ca
2. **Copy the board URL** from the browser while on the **Board**:
   `https://<team>.atlassian.net/jira/software/projects/<KEY>/boards/<N>`
3. **Submit that board link** on Brightspace (an epic link opens only that one work item)

<!-- pause -->

> **Please don't remove the TAs before grades are out.**

<!-- end_slide -->

Jira 11: Common Mistakes + Further Reading
===

### Common mistakes

- Kanban space: no sprint, no sprint goal
- Sprint created but **never started**
- One shared account → no individual history
- Everything moved to Done on the last day
- Stand-ups missing, or not every member has done / doing / blocked
- Two people "on" one task, but only one shows as assignee
- Roles not visible, or not rotated
- Board link that the TA **couldn't open**

### Further reading (official Atlassian)

- Scrum with Jira (step by step): https://www.atlassian.com/agile/tutorials/how-to-do-scrum-with-jira
- Sprints: https://www.atlassian.com/agile/tutorials/sprints
- Backlog: https://support.atlassian.com/jira-software-cloud/docs/use-your-scrum-backlog/
- Story vs Task (work types): https://www.atlassian.com/software/jira/guides/issues/overview
- Add people: https://support.atlassian.com/jira-software-cloud/docs/add-people-to-team-managed-projects
- Roles on Free: https://support.atlassian.com/jira-software-cloud/docs/next-gen-permissions/
- Free plan: https://support.atlassian.com/jira-cloud-administration/docs/explore-jira-cloud-plans/

<!-- end_slide -->
