---
title: "SYSC 3020: Introduction to Software Engineering"
sub_title: "Assignment 4: Design (Patterns & Modular Quality) · Lab Walkthrough"
author: "Rinkesh Joshi · rinkeshjoshi@cmail.carleton.ca"
theme:
  name: catppuccin-latte
---

SYSC 3020: Introduction to Software Engineering
===

### Assignment 4: Design (Patterns & Modular Quality) · Lab Walkthrough

**Fall 2026**

**TA:** Rinkesh Joshi · rinkeshjoshi@cmail.carleton.ca

**Lab:** LE1 · Wednesday, November 18, 2026 · 2:35 PM to 5:25 PM

**Room:** Mackenzie Building 4233

**Assignment due:** Saturday, November 28, 2026 by 11:55 PM

**Weight:** 8% of final grade · graded out of 16

<!-- end_slide -->

The Three Tasks at a Glance
===

<!-- column_layout: [1, 1, 1] -->

<!-- column: 0 -->

### Task A
## Patterns

Find **3 design patterns** that
already exist in the code.

- From the Lecture 8 list
  (7 patterns)
- ≥ 1 behavioural
- ≥ 1 creational or structural
- Per pattern: diagram, roles,
  code reference, why it helps

**Output:** 3 pattern write-ups
+ 3 design class diagrams

<!-- column: 1 -->

### Task B
## Correctness

Compare each pattern with
the **standard** (Lecture 8).

- **Part 1:** match and
  differences. Does the
  variation suit JPacman?
- **Part 2:** one place of
  your own where a pattern
  could help, or is applied
  imperfectly

**Output:** 3 comparisons
+ 1 improvement case

<!-- column: 2 -->

### Task C
## Modular Quality

Judge **2 classes or packages**,
then test the judgement.

- Judgement → evidence →
  interpretation
- Checkstyle + PMD reports
- Coupling + cohesion
- ≥ 2 OO principles
- An **RFC** (design-change
  proposal)

**Output:** analysis + RFC

<!-- reset_layout -->

Plus **Sprint 4** in **Jira** across all tasks (planning, stand-ups, board, review + retro).

> **New in A4:** stand-ups go under four stand-up tasks, "A4 – Standup 1" to "A4 – Standup 4" (see the Sprint 4 slides).

<!-- end_slide -->

What You Submit
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Deliverables (one per team, on Brightspace)

1. **design-report.pdf**, exported from Confluence
   - Patterns (Task A)
   - Pattern correctness (Task B)
   - Modular-quality analysis (Task C)
   - Design rationale (RFC)
   - Team & process (roles, retro, AI Usage note)

2. **uml-sources.zip** with your PlantUML `.puml`
   design class diagrams

3. **Jira board link**, with the instructor
   and all the TAs added so that it opens

These three items only. As in A2 and A3, list
every team member (name + student ID)
in the Brightspace submission.

<!-- column: 1 -->

### Penalties to Watch

- Missing design-report.pdf → **−3 marks**
- Missing uml-sources.zip → **−3 marks**
- Jira link we cannot open → **−3 marks**
- Late → **−15% of the full grade per day**
  (accepted up to 48 h late)
- Individual: fewer than 2 stand-up comments
  in a week → **−1 mark** for that week (max −2)

### Presentation

A random sample of students may be asked
to present. It must match what you submitted.
Can't explain it → affects your individual grade.

<!-- reset_layout -->

Adjustments are applied in this order: rubric total minus missing items, late penalty, presentation result (if selected), your stand-up deduction.

> **Deadline:** Saturday, November 28, 11:55 PM.

<!-- end_slide -->

Grading Rubric: Quick View
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Pattern Identification (4 pts)
Tasks A and B together. Three patterns across the
required categories, correctly identified and justified
with a **standard-vs-variation** argument, code evidence,
and why each is useful here. Your own improvement
case (Task B, Part 2) is clearly argued.

### Modular-Design Analysis (4 pts)
Design judgement **stated first**, then tested against
static-analysis evidence and interpreted in context.
Coupling, cohesion and ≥ 2 OO principles in depth,
with concrete improvement reasoning.

<!-- column: 1 -->

### Design Rationale: RFC (4 pts)
Clear RFC with at least one **alternative**, explicit
**trade-offs** (what improves and what gets worse),
and a justified decision.

### Process & Reporting (4 pts)
Jira board current with real sprint activity
(stand-up comments from **every member**, roles
rotated, role labels). Retrospective present and
AI usage disclosed. Report complete and correctly
formatted (unrendered diagrams cost marks).

<!-- reset_layout -->

| Score Range | Meaning |
|---|---|
| 14-16 | Excellent work |
| 10-13 | Good work |
| 6-9 | Some improvement needed |
| 0-5 | Much improvement needed |

Each criterion scores 0 to 4. It scores 0 only if the work for it is missing entirely.

<!-- end_slide -->

From A3 to A4: What Changes
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Reuse from Earlier Assignments

- **CD-01** and **SD-01 … SD-03** (A2): classes,
  operations, who calls whom
- **DV-01** (A3): package imports, your first
  coupling evidence
- **ADRs** (A3): the RFC has a similar shape
- PlantUML, same Jira space and accounts.
  Instructor + TAs are already added
- Penalties: 15%/day, −3 per missing item

<!-- column: 1 -->

### New or Different

- Report is now **design-report.pdf**.
  Weight is **8%** (A2 and A3 were 5%)
- Task A scope: `ui`, `sprite`, `Launcher`
- **Checkstyle** and **PMD**, already in the build.
  Update your copy of the starter first
- Stand-ups under **four stand-up tasks**
- An **RFC**: a proposal, no code changes
- Not asked this time: debugger screenshots,
  an RTM section

<!-- reset_layout -->

<!-- end_slide -->

Before You Start › Lecture Notes
===

### Go through the posted slides first and use their vocabulary

| Slides | Covers | Use it for |
|---|---|---|
| **Lecture 8:** Design Patterns | intent, structure and roles of each pattern | Tasks A, B |
| **Lecture 7:** Modular Design | coupling, cohesion, OCP, DIP, ISP, Law of Demeter | Task C |
| **Checkstyle and PMD Tutorial** (Brightspace) | run the tools, read a finding, rules and limits | Task C |

<!-- pause -->

### Where the "standard structure" is (Lecture 8 slide numbers)

| Singleton | Builder | Adapter | Façade | Observer | Strategy | State |
|---|---|---|---|---|---|---|
| 8-10 | 11-12 | 14-15 | 16-18 | 21-23 | 24-26 | 27-30 |

Also useful: **Comparing Patterns** (slide 19) and **Pattern Selection** (slide 31).

The RFC is not in the lectures. The handout's layout is enough (see the RFC slide).

<!-- end_slide -->

Before You Start › References & Links
===

### On the course page

1. SOLID in plain English: https://www.freecodecamp.org/news/solid-principles-explained-in-plain-english/
2. Abstract Factory, UML class diagram example: https://www.uml-diagrams.org/design-pattern-abstract-factory-uml-class-diagram-example.html

### For A4

3. PMD Java design rules: https://pmd.github.io/pmd/pmd_rules_java_design.html
4. Checkstyle: https://checkstyle.org
5. PlantUML class diagrams: https://plantuml.com/class-diagram
6. Design Patterns Explained Simply (Lecture 8 references): https://sourcemaking.com/design-patterns-ebook

<!-- pause -->

| Link | Use it for | Careful |
|---|---|---|
| **1** SOLID | plain words + code for OCP, DIP, ISP | no Demeter, and S and L\* are not in your four |
| **2** Abstract Factory | how a pattern is drawn with its roles | Factory patterns do not count for Task A |
| **3** PMD rules | what each rule measures | the limits are this project's (tutorial, section 6) |
| **6** SourceMaking | a second explanation of a pattern | name the roles as Lecture 8 does |

\*S and L are Single Responsibility and Liskov Substitution.

<!-- end_slide -->

Sprint 4 › Run It in Jira
===

### Day 1: Sprint planning

- Once A3 is submitted, complete Sprint 3 (Board → **Complete sprint**), then plan Sprint 4
- Create the epic **"A4: Design: Patterns & Modular Quality"** (a new epic, same Jira space)
- Break it into tasks and assign each (shared task → sub-tasks, Jira Guide › Jira 4)
- Create the **four stand-up tasks** (next slide)
- **Create Sprint** → drag all the tasks in → one-line **sprint goal** → **Start Sprint** (end date = the due date)
- Tag every work item with its assignee's **role label** (Jira Guide › Jira 5):
  `role-ProductOwner` · `role-ScrumMaster` · `role-QALead`

<!-- pause -->

### Rotate roles (no one keeps a role two sprints running)

| Member | Sprint 1 (A1) | Sprint 2 (A2) | Sprint 3 (A3) | Sprint 4 (A4) |
|---|---|---|---|---|
| A | Product Owner | Scrum Master | QA Lead | **Product Owner** |
| B | Scrum Master | QA Lead | Product Owner | **Scrum Master** |
| C | QA Lead | Product Owner | Scrum Master | **QA Lead** |

With three roles, Sprint 4 can return you to your Sprint 1 role. That is allowed.

<!-- pause -->

### During the sprint + last day

- Move tasks **Backlog → In Progress → Done** as you work. The board history is graded
- Last day: review + 3 bullets (keep / change / try) in the **Team & process** section
- The instructor (kahani@sce.carleton.ca) and all TAs stay added to the space

<!-- end_slide -->

Sprint 4 › Stand-ups: Four Tasks, One Comment Each
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Create these four tasks (in the sprint)

```
Epic  A4: Design: Patterns & Modular Quality
├─ Task  A4 – Standup 1
├─ Task  A4 – Standup 2
├─ Task  A4 – Standup 3
├─ Task  A4 – Standup 4
├─ Task  Task A: pattern 1 …
└─ …
```

### Each comment (name + date, then three lines)

```
Sam (QA Lead), <date>
Done:    listed the candidate patterns.
Doing:   drawing the class diagram for pattern 1.
Blocked: cannot find where the object is created.
```

<!-- column: 1 -->

### The rule (handout)

- Every member posts **at least one comment
  under each of the four tasks**
- From your own account
- On four different days: Standup 1 and 2 in
  Week 1, Standup 3 and 4 in Week 2
- Comments for Standup 2 go under
  "A4 – Standup 2", and so on

### What we count

3 members × 4 tasks = **12 comments**, minimum.
Fewer than 2 in a week costs you 1 mark of
your own for that week (at most 2).

### Suggested

- Assign the four tasks to the Scrum Master
- Move a stand-up task to Done once all three
  of you have commented
- Blocked can be "None"

<!-- reset_layout -->

> When you hold each stand-up is your team's decision.

<!-- end_slide -->

Setup › Update Your Copy of the Starter
===

The starter's **`pmd-rules.xml` was updated for A4** (complexity, coupling and size rules).
With an older copy, PMD reports next to nothing and Task C has no evidence to quote.

### Pick one way (each gives you the same file)

- **Git clone:** run `git pull` in the repo folder. If Git refuses because of local changes, run `git stash`, then `git pull` again
- **ZIP download:** replace only `pmd-rules.xml` (below), or download the ZIP again and work in the new folder
  (macOS: `chmod +x gradlew`)

<!-- pause -->

### Replace just `pmd-rules.xml` (run in the folder with `build.gradle`)

```bash
# macOS (Windows: the same command on ONE line, with curl.exe instead of curl)
curl -L -o pmd-rules.xml \
  https://raw.githubusercontent.com/SYSC3020-F2026/sysc-termproject-starter/HEAD/pmd-rules.xml
```

Without a terminal, open `pmd-rules.xml` in the repo on GitHub, use **Download raw file**, and save it over the old one in the project root.

### Check that you have the A4 rules (in the project root)

```bash
# macOS: prints 9
grep -c "design.xml" pmd-rules.xml
# Windows: prints 9 lines
findstr /c:"design.xml" pmd-rules.xml
```

<!-- end_slide -->

How You Work › Diagrams-as-Code (Again)
===

### Same pipeline as A2 and A3

```
dp-01.puml ──render──▶ DP-01.png ──upload──▶ Confluence page ──export──▶ design-report.pdf
     │
     └───────────────────────── zip all .puml ──────────────────────▶ uml-sources.zip
```

<!-- pause -->

### Give every diagram and record an ID (suggested scheme)

| ID | What | File |
|---|---|---|
| **DP-01 … DP-03** | Design class diagram, one per pattern (Task A) | `dp-01.puml` … |
| **IC-01** | Your improvement case (Task B, Part 2), text | on the page |
| **RFC-01** | Design rationale (Task C), text | on the page |

Task B refers back to the diagrams by ID ("see DP-02") instead of copying them.

<!-- pause -->

> Class diagrams need **Graphviz** to render. The PlantUML web server (https://www.plantuml.com/plantuml/uml/) needs no install. With a local PlantUML and no Graphviz, add `!pragma layout smetana` right after `@startuml` (setup steps: A2 slides).

<!-- end_slide -->

Task A › Rules and Scope
===

### The rules for your three patterns

- Three **different** patterns from the list on the next slide, each **already in the code**.
  A pattern you only propose (Task B) does not count
- At least one **behavioural**, and at least one **creational or structural**

<!-- pause -->

### Where to look

```
src/main/java/nl/tudelft/jpacman/
├── Launcher.java   ← in scope
├── ui/             ← in scope (7 files)
├── sprite/         ← in scope (6 files)
└── board/ game/ level/ npc/ points/
                    ← only "the classes they use directly" (e.g. Level, Game, PointCalculator)
```

In practice, start from the imports. Same-package classes need no import, so this search misses them:

```bash
# macOS
cd src/main/java/nl/tudelft/jpacman
grep -h "^import nl.tudelft.jpacman" ui/*.java sprite/*.java Launcher.java | sort -u
# Windows
cd src\main\java\nl\tudelft\jpacman
findstr /c:"import nl.tudelft.jpacman" ui\*.java sprite\*.java Launcher.java
```

<!-- end_slide -->

Task A › The Seven Patterns: Standard Roles (Lecture 8)
===

**Creational:** Singleton · Builder   **Structural:** Adapter · Façade   **Behavioural:** Observer · Strategy · State

Factory, Template Method and Command do not count for Task A.

| Pattern | Intent, in short | Roles on the slide | Slide |
|---|---|---|---|
| **Singleton** | one instance, one global access point | `Singleton`: private constructor, `getInstance()` | 9 |
| **Builder** | build a complex object step by step | Director · Builder · ConcreteBuilder · Product | 12 |
| **Adapter** | give an object the interface clients expect | Client · Target · Adapter · Adaptee | 15 |
| **Façade** | one simple interface over a subsystem | Client(s) · Façade · subsystem classes | 17 |
| **Observer** | dependents notified when the subject changes | Subject · Observer · a Concrete class of each | 22 |
| **Strategy** | interchangeable family of algorithms | Client · Context · Interface · Implementation | 25 |
| **State** | behaviour follows an internal state object | Context · State · ConcreteState | 28 |

<!-- pause -->

### Reading the slides

- The class diagram on each slide is the "standard structure" that Task B compares against
- Note the operations too: `attach()` / `detach()` / `notify()` and `update()` (Observer),
  `construct()` / `buildPart()` / `getResult()` (Builder), `handle()` (State), `algorithm()` (Strategy)
- Slide 19 separates look-alikes: "Façade defines a new interface", "Adapter reuses an old interface"

<!-- end_slide -->

Task A › Finding a Pattern in the Code
===

| Pattern | Ask | Signs to look for in the code |
|---|---|---|
| Singleton | exactly one instance, reachable everywhere? | private constructor + a static access method |
| Builder | a complex object built step by step? | a Director that calls build steps on a separate Builder |
| Adapter | right stuff, wrong interface? | implements what clients expect, forwards elsewhere |
| Façade | one tidy front for several related objects? | clients call one class that coordinates several others |
| Observer | must objects know about events elsewhere? | a collection of listeners, a register method, a loop |
| Strategy | rules or algorithms that vary by context? | interface held in a field, implementation set outside |
| State | a state machine built from objects? | work delegated to a "current state" object |

<!-- pause -->

### Search first, then read the code (in the source folder: `cd` as on the *Rules and Scope* slide)

```bash
# macOS: who declares / implements / extends what, and what is static
grep -rnE "(interface|implements|extends) " ui sprite Launcher.java
grep -rn "static " ui sprite Launcher.java
# Windows
findstr /n "interface implements extends" ui\*.java sprite\*.java Launcher.java
findstr /n /c:"static " ui\*.java sprite\*.java Launcher.java
```

<!-- pause -->

> **Hint:** Start where the program starts (`main`) and ask what each object is for.

<!-- end_slide -->

Task A › Traps
===

| It looks like | Before you claim it, show (Lecture 8 slides) |
|---|---|
| a class name with a pattern word in it | the roles, in code |
| a `static final` field | Singleton: a private constructor and one access point (slide 9) |
| a `boolean` flag | State: separate state objects (slide 28) |
| an interface | Strategy: who holds it, and how the implementation is chosen |
| a class with many dependencies | Façade: its clients, and the subsystem it hides from them |
| a class that forwards calls | Adapter: a changed interface (slides 14-15) |

<!-- pause -->

JPacman need not contain all seven patterns, so don't force one onto code that lacks its structure.
Rubric Level 1 reads: "Patterns missing, mislabelled, or invented."

<!-- end_slide -->

Task A › What You Hand In per Pattern
===

| # | What | Notes |
|---|---|---|
| 1 | **Design class diagram** (PlantUML) | only the classes and interfaces that form the pattern |
| 2 | **Roles** | for every class in the diagram, its role in the standard pattern |
| 3 | **Code reference** | file path, class, method or field, line numbers |
| 4 | **Why it is useful here** | 1-2 sentences about JPacman: what would be harder without it |

<!-- pause -->

### The handout's sample (`Foo`, `Bar`, `Baz` are made-up classes)

```
Pattern 1: Observer (behavioural)                                  diagram: DP-01
Roles
  Foo   Subject             keeps the list of listeners and notifies them
  Bar   Observer            the interface (declares the method that gets called)
  Baz   concrete observer   implements Bar and reacts
Code reference
  src/main/java/.../Foo.java, Foo.notifyListeners(), lines 40–52
Why it is useful here
  Without this pattern, Foo would have to know every class that needs updating,
  and adding a new one would mean editing Foo.
```

A real code reference: `src/main/java/.../Level.java`, `Level.start()`, lines 201–210.

**How a claim is marked.** **Intent:** does the code solve the problem the pattern is meant to solve? **Structure and behaviour:** does it
contain the essential collaborations, even if some participants are combined or omitted? **Evidence:** real
methods, fields and relationships, accurate code references, variations explained. A valid variation is accepted.

<!-- end_slide -->

Task A › The Pattern Diagram: What to Show
===

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### In

- The classes and interfaces that form the
  pattern, and nothing else
- Their relationships: inheritance,
  implementation, association, dependency
- Per class, only the fields and methods
  **relevant to the pattern**, with visibility
- Multiplicities only where they matter
  (one subject, many listeners)

### Out

- The whole system
- Getters, helpers and fields that play no part
  in the pattern

<!-- column: 1 -->

### Notation, as in A2

- Visibility: `+` public · `-` private ·
  `#` protected · `~` package-private
- A field whose type is a project class →
  association with role name (= field name)
- `«interface»`, dashed realization,
  abstract classes and operations marked
- Operations: `+ name(param : Type) : Return`

### A role played by an outside type

A role may be played by a type from outside
the project. Draw a name-only box (plus the
one operation that matters) and say so in
your Roles list.

<!-- reset_layout -->

The roles go in your text. A `note right of Foo : Subject` in the diagram also helps the reader.

<!-- end_slide -->

Task A › The Handout's Example, Started (DP-01)
===

<!-- column_layout: [3, 2] -->

<!-- column: 0 -->

```
@startuml DP-01
skinparam classAttributeIconSize 0
hide circle
hide empty members
class Level {
  + addObserver(observer : LevelObserver) : void
  + removeObserver(observer : LevelObserver) : void
  - updateObservers() : void
}
interface LevelObserver <<interface>> {
  + levelWon() : void
  + levelLost() : void
}
' the field Level.observers, as an association
Level --> "0..*\n-observers" LevelObserver
' TODO: which class implements LevelObserver?
'       Add it, with the operations that matter
' TODO: who registers the observer, and where?
' TODO: which concrete class runs? In or out?
@enduml
```

<!-- column: 1 -->

### What the handout says

"`Level` notifies interested objects
through the `LevelObserver` interface
(the **Observer** pattern, which is
behavioural)."

You may use it as one of your three
if you document it fully. Then find
two more, at least one of them
creational or structural.

### Notice

- `observers` is a field holding
  project objects, so it is drawn as an
  association, `0..*` (the set starts empty)
- `LevelObserver` has no file of its
  own. Look inside `Level.java`
- Verify every member against
  the code

<!-- reset_layout -->

(A syntax demo only. The TODOs, the roles, the code reference and the "why" are yours.)

<!-- end_slide -->

Task B › Part 1: Compare Each Pattern with the Standard
===

For each of your three patterns, write two items:

1. **Match:** how closely the JPacman code follows the standard structure on the Lecture 8 slide
2. **Differences:** what is different, if anything. A difference is not automatically a problem.
   Say whether it suits JPacman and why.

<!-- pause -->

### One row per standard role (made-up names)

| Standard role | In the code | Same or different | Evidence |
|---|---|---|---|
| Subject | `Foo` | same | `Foo.java`, method, lines … |
| Observer (interface) | none: `Foo` calls `Bar` directly | **different:** interface missing | … |
| ConcreteObserver | `Bar` | … | … |

<!-- pause -->

### Differences worth checking

- A role is missing, or one class plays two roles
- An abstract class where the slide has an interface (or the reverse), or a nested type
- A role with no named class of its own
- Different operations from the ones on the slide
- Who creates and connects the objects, and when

Refer to Task A by ID ("see DP-02") instead of copying it, and add a code reference for any code you discuss
here for the first time. If the code matches the standard exactly, say so and explain why no variation was needed.

<!-- end_slide -->

Task B › Part 2: Find One Place to Improve
===

### One case of your own, of either kind

- a Lecture 8 pattern **could improve the design** but is not used there, or
- a pattern that is used there is applied **imperfectly**

Then argue whether the change is worth making, with at least one benefit and at least one cost.
It is fine to conclude that the change would not be worthwhile.

<!-- pause -->

### The handout's worked example (does not count as yours)

`inProgress` is a boolean, not State objects. For: `start()` / `stop()` already behave differently by state.
Against: only two states, few checks, new classes for very little behaviour. Model your case on its for / against lists.

<!-- pause -->

### Format (IC-01)

```
IC-01: <pattern> for <place in the code>
Where:    class.method (file path, lines)
Today:    what the code does now
Change:   which Lecture 8 pattern, and which class would play which role
Benefit:  at least one, concrete (what becomes easier to change or test)
Cost:     at least one, concrete (new classes, indirection, risk)
Verdict:  worthwhile or not, and why
```

> **Hint:** Lecture 8, slide 31 (*Pattern Selection*) gives a question for five of the seven patterns (not Singleton or Builder). Find a place in the code where the answer is yes but that pattern is not used.

<!-- end_slide -->

Task C › Three Steps, in Order
===

1. **Design judgement (before the tools).** From the code, pick **two classes or packages** with particularly
   good or questionable modularity (two good, two questionable, or one of each), and explain why
2. **Static-analysis evidence.** Run Checkstyle and PMD and check whether the findings support or contradict you
3. **Interpretation.** Explain what the findings mean in context. A high metric alone is **not** a design defect.

<!-- pause -->

### Then, for the same two

- **Coupling** and **cohesion** for each of the two
- At least two of {Open–Closed, Dependency Inversion, Interface Segregation, Law of Demeter},
  analysed across the two together
- An **RFC** to close

<!-- pause -->

### Which classes

The Task A scope is about patterns. The handout sets no package limit for Task C, so your A2 and A3 models
of the core packages apply. If a model differs from the code, trust the code.

<!-- end_slide -->

Task C › Run Checkstyle and PMD
===

Open a terminal in the project root (the folder that contains `build.gradle`).

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Windows

```bash
.\gradlew.bat check --continue

# open the reports
start build\reports\pmd\main.html
start build\reports\checkstyle\main.html
```

<!-- column: 1 -->

### macOS

```bash
./gradlew check --continue

# open the reports
open build/reports/pmd/main.html
open build/reports/checkstyle/main.html
```

<!-- reset_layout -->

<!-- pause -->

### What to expect

- The first run downloads libraries and takes a few minutes
- Keep `--continue`. Without it Gradle stops at the first failed check and the PMD report may never be created
- **"BUILD FAILED" is expected.** PMD fails the build when it finds violations. In our run `pmdMain` reported
  **98**. Far fewer means you still have the old `pmd-rules.xml` (*Setup* slide)
- A JPacman window opens by itself for a moment while the tests run, then closes
- Check that both report folders contain a report, and write in your report which tools produced one

<!-- end_slide -->

Task C › Open and Read the Reports
===

| Tool | Folder | Open |
|---|---|---|
| Checkstyle | `build/reports/checkstyle/` | `main.html` in a browser |
| PMD | `build/reports/pmd/` | `main.html` in a browser |

The `test` and `defaultTest` reports in the same folders cover the test code. They are not your evidence.

<!-- pause -->

### The PMD table has four columns: **#** · **File** · **Line** · **Problem**

- **Problem** is the message. The rule name is not a column. The message is a link that ends in the rule name
  (`…#ncsscount`), and `main.xml` has it as `rule="NcssCount"`
- The table is sorted by file. Press **Ctrl+F** and type your class's file name (`Foo.java`) to jump to its rows

<!-- pause -->

### What the messages look like (PMD 6.8.0, the wording depends on the PMD version)

| Rule | Message | Number? |
|---|---|---|
| `CyclomaticComplexity` | The method 'x(List)' has a cyclomatic complexity of 12. | yes |
| `CyclomaticComplexity` | The class 'X' has a total cyclomatic complexity of 30 (highest 8). | yes |
| `NcssCount` | The class 'X' has a NCSS line count of 75 (Highest = 20). | yes |
| `CouplingBetweenObjects` | High amount of different objects as members denotes a high coupling | **no** |
| `ExcessiveImports` | A high number of imports can indicate a high degree of coupling … | **no** |

`X`, `x` and the numbers are placeholders. "highest" is the worst single method of the class. Where the message
has no number, count it yourself (the imports, the different types the class uses) and cite the code.

<!-- end_slide -->

Task C › The Rules and Their Limits
===

| Rule | Limit in this project | A signal for |
|---|---|---|
| `CyclomaticComplexity` | method **10** · class **25** | complexity, testability |
| `NPathComplexity` | 200 (PMD default) | complexity, testability |
| `NcssCount` | method **20** · class **60** statements | size, cohesion |
| `CouplingBetweenObjects` | **10** types | coupling |
| `ExcessiveImports` | **15** imports | coupling |
| `TooManyMethods` · `TooManyFields` | **10** methods · **15** fields | cohesion |
| `GodClass` | a combination of metrics | cohesion |
| `LawOfDemeter` | no limit, flags call chains | see the next slide |
| Checkstyle `MethodLength` | **30** lines | size |

These limits are listed in the Checkstyle and PMD Tutorial (sections 5 to 7). For some rules a value equal to the limit is already reported,
for example a method with complexity exactly 10. To see exactly what a rule counts, click its message in the report (the PMD 6.8.0 page for that rule).

<!-- pause -->

### Be able to explain these two

- **Cyclomatic complexity** is the number of decisions (`if`, `for`, `while`, `case`, `&&`, `||`) plus one.
  Three `if`s and one loop give 3 + 1 + 1 = 5 paths to test
- **NCSS** counts non-commenting source statements, that is, the real statements without comments and blank lines

<!-- pause -->

Expect an (almost) empty Checkstyle report for `main`, and say so in your report.

> A metric is a signal, never a proof. Use it to test your judgement. (Checkstyle and PMD Tutorial, section 7)

<!-- end_slide -->

Task C › Two Things That Can Mislead You
===

### 1. A suppressed rule reports nothing

Some classes carry `@SuppressWarnings("PMD.…")`. The handout names `Level`, `Launcher` and `Board`.
PMD does not report those rules for them, and the handout counts a suppression as evidence.

```bash
# macOS (project root)
grep -rn "PMD\." src/main/java
# Windows (project root)
findstr /s /n /c:"PMD." src\main\java\*.java
```

For each hit in your two classes, name the rule and the place (file + line), read what the rule counts (link 3),
count it in the class the same way, and say what you conclude.

<!-- pause -->

### 2. `LawOfDemeter` fires almost everywhere

- In our run, **87 of the 98** findings for `main` were `LawOfDemeter`, ordinary getter chains included
- A long list of hits is not by itself evidence of a design problem
- Pick the specific chains you can defend as a real "reach through" (Lecture 7, slide 8) and show the code

<!-- pause -->

> No findings means that no enabled rule flagged a violation. It does not by itself show good modularity.

<!-- end_slide -->

Task C › Step 1: Design Judgement (Before the Tools)
===

### The vocabulary (Lecture 7, slide 3)

- **Cohesion:** The degree to which the elements inside a module belong together. Aim for high cohesion.
- **Coupling:** The degree to which a module depends on other modules. Aim for low coupling.
- Signs (slide 4): more than one reason to change = low cohesion, uses many other types = high coupling

<!-- pause -->

### Questions to ask of a class

- Can you state its job in one sentence without "and"?
- How many other project classes does it name (imports, field types, parameters)?
- Who depends on it, and who would have to change if it changed?

### Questions to ask of a package

- Which packages does it import, and does any of them import it back? Your **DV-01** (A3) shows this
- For a package, your evidence is its imports plus the findings for the classes inside it

<!-- pause -->

### Quick facts before the tools (in the source folder: `cd` as on the *Rules and Scope* slide)

```bash
# macOS: prints the number of imports of one file (same-package classes are not in it)
grep -c "^import" level/Level.java
# Windows: lists the imports, so count the lines
findstr /b /c:"import " level\Level.java
```

Write the judgement down before you run the tools. Two good, two questionable, or one of each are all fine.

<!-- end_slide -->

Task C › Steps 2 and 3: Evidence, Then Interpretation
===

### Step 2: quote the evidence (made-up class and numbers, from the tutorial)

| Tool | Rule | Where | Value (limit) |
|---|---|---|---|
| PMD | CyclomaticComplexity | `Foo.load()` | 14 (10) |
| PMD | TooManyMethods | `Foo` | 18 methods (10) |
| Checkstyle | MethodLength | `Foo.draw()` | 52 lines (30) |

Cite it in a sentence: "PMD reports a CyclomaticComplexity of 14 for `Foo.load()` (limit 10)."

<!-- pause -->

### Step 3: say what it means for your judgement

| You judged | The tools say | Write |
|---|---|---|
| questionable | findings | they **support** the judgement. Say which finding matches which concern |
| questionable | nothing | "The tools do not flag this concern. Our judgement rests on the code evidence." |
| good | findings | they **contradict** it: either the size is justified in context, or you revise |
| good | nothing | consistent, but not proof. Back it with code evidence too |

<!-- pause -->

Explain the number as well: say what makes the method complex and whether a split would reduce it.
The handout's example of a justified size: "a coordinating class like `Level` may justifiably be larger".

<!-- end_slide -->

Task C › Coupling, Cohesion and the Principles
===

Evaluate coupling and cohesion for **each** of your two. Then analyse **at least two** of these four across the two together:

- **Open–Closed** (Lecture 7, slide 5): "open for extension, but closed for modification."
  *Look for:* to add a new kind of thing, do you add a class, or edit an existing `if` / `switch`?
- **Dependency Inversion** (slide 6): "Design to an interface, not an implementation".
  *Look for:* fields and parameters typed by an interface, or `new Concrete…()` inside a high-level class?
- **Interface Segregation** (slide 7): "No client module should be forced to depend on methods it does not use."
  *Look for:* empty method bodies in an implementation, or clients that use only part of an interface
- **Law of Demeter** (slide 8): "Only talk to your immediate friends".
  *Look for:* `b.getC().doIt()` inside A, where A reaches through B to use C

<!-- pause -->

### The handout's example

You judge classes `A` and `B`. You evaluate coupling and cohesion for both, then analyse Open–Closed with code
from `A` and Law of Demeter with code from `B`. You do not have to apply every principle to both.

<!-- pause -->

### Keep in mind

- A principle can be respected or violated. Either way, give code references
- **Single Responsibility** is not one of the four you choose from. Slide 4 covers its idea under low cohesion
- "In depth" means what the code does, why that respects or breaks the principle, and what follows for a future change

<!-- end_slide -->

Task C › The RFC (Design Rationale)
===

An **RFC** (Request for Comments) is a short design-change proposal. Take one weakness you found (an imperfect
or absent pattern, or a modularity smell), propose a change, and weigh it against at least one alternative.

```
RFC-01: <title>
Problem:      what is wrong now, with a code reference and, if available, a PMD value
Proposal:     what you would change
Alternative:  another approach (keeping the current design counts), with its benefits and costs
Trade-offs:   what improves (for example, fewer responsibilities per class)
              what becomes worse (for example, more classes to maintain)
Decision:     which option you choose, and why
```

<!-- pause -->

### Rules (handout)

- The RFC must propose a **concrete change**. The decision may be to adopt it, to adopt the alternative,
  or to keep the current design, as long as the trade-offs justify it
- State explicitly **what improves and what becomes worse** or more complicated
- You may use your Task B weakness as the topic. Task B asks whether a change is worthwhile. The RFC works
  one specific proposal out in detail
- The RFC is a proposal only. You do not need to change the JPacman code

<!-- pause -->

| Record | ADR (A3) | RFC (A4) |
|---|---|---|
| About | a decision already in the code | a change you propose |
| Ends with | consequences of what exists | a decision: adopt, alternative, or keep |

<!-- end_slide -->

The Design Report Page in Confluence
===

### Confluence → Create → Blank page, e.g., **"Design Report: JPacman Patterns & Modular Quality"**

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

### Sections

1. **Patterns** (Task A): DP-01 … DP-03 and
   their write-ups
2. **Pattern correctness** (Task B): the three
   comparisons + your improvement case
3. **Modular-quality analysis** (Task C): the
   three steps, coupling and cohesion,
   the principles
4. **Design rationale (RFC)**
5. **Team & process**: team roles, retro
   (keep / change / try), AI Usage note

<!-- column: 1 -->

### Embedding diagrams

- Type `/image` → upload the rendered PNG
- One image per diagram, captioned with its ID
- No raw PlantUML text instead of a picture

### Quoting findings

Copy each finding into a table (tool, rule,
where, value and limit).

### AI Usage note

Whether you used AI tools, how, and for what.
Any outside source too.

### Export

Page → **⋯** → **Export** → **PDF**
→ rename to **design-report.pdf**

<!-- reset_layout -->

<!-- end_slide -->

Self-Check Before You Submit
===

- □ **3 different patterns** from the Lecture 8 list: ≥ 1 behavioural, ≥ 1 creational or structural, all already in the code
- □ Each pattern has a design class diagram, roles for every class, a code reference (file path, class, method or field, line numbers) and 1-2 sentences on why it helps here
- □ Task B: for each pattern, how closely it matches the standard and what is different, with a verdict
- □ Task B: **one place of our own** (not the State example), with a benefit, a cost and a conclusion
- □ Task C: both tools produced reports, and the report says so. `PMD.` suppressions checked
- □ Task C: the three steps in order (judgement, evidence, interpretation)
- □ Task C: coupling and cohesion for each of the two, and **≥ 2 OO principles** in depth
- □ **RFC**: a concrete change, an alternative, what improves and what gets worse, a decision
- □ **Team & process** section: roles, retro, AI Usage note
- □ **uml-sources.zip** has every `.puml`, and every diagram in the report is rendered
- □ Jira: epic, assigned tasks with role labels, a comment from **every member under each of the four "A4 – Standup" tasks**. Instructor + all TAs added, and the link opens
- □ Submitted on Brightspace: design-report.pdf + uml-sources.zip + board link, with all names + student IDs

<!-- pause -->

> **Remember:** work that is not clearly explained or not traceable to the actual code will not be considered correct. Any team member may be asked to present it.

<!-- end_slide -->

Troubleshooting
===

| Problem | What to do |
|---|---|
| Java version / unsupported class file error | not on **JDK 11**: `java -version` (A1 slides) |
| `./gradlew: Permission denied` (macOS) | `chmod +x gradlew`, once |
| `gradlew.bat` is not recognized (Windows) | type `.\gradlew.bat`, with the leading `.\` |
| No PMD report | you left out `--continue`, so run it again |
| Only `main.xml`, no `main.html` | open the `.xml` in a browser or text editor |
| Build fails with **test** errors | ignore them and confirm both tools produced reports |
| Nothing reported for a class you expected | look for `@SuppressWarnings("PMD.…")` on it |
| Class diagram does not render | PlantUML web server, or `!pragma layout smetana` |
| We could not open your Jira link | add instructor + TAs and submit the **board** URL |

<!-- pause -->

### More help

Ask in the lab, on Discord or Brightspace, or by email: rinkeshjoshi@cmail.carleton.ca
