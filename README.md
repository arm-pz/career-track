# career-track

An agent skill for the moves around a career: the positioning line you can repeat, the case for the next level, a performance-review self-assessment written from your own facts, an executive-presence read of the rooms where it is going wrong, a salary or promotion script, a pivot path with its friction points, a network map with dates, preparation for the interviews inside your own employer (a promotion panel, a review conversation), and a plan with this week's actions and ninety-day milestones. It writes only from what you supply. Where a quantified result would help and you have not given one, it leaves `[metric — supply this]` and collects the gaps, so nothing in your case is a number you cannot defend in the meeting.

Install: `npx skills add arm-pz/career-track --skill career-track`

Ask it things like:

- "I have been at senior for three years, how do I actually get promoted?"
- "Write my performance-review self-assessment from these notes about what I did."
- "I need to ask for more money. What do I establish before I name a number?"
- "I want to move from support into product. What is the shortest route and what will slow me down?"

## What you get

| Mode | Output |
|---|---|
| Promotion case | The level bar as you report it, evidence mapped per criterion, gaps, counter-case, and the script for the conversation |
| Self-assessment | Drafted sections in your form's shape, plus **Slots to close** and **Not claimed** |
| Positioning and visibility | The line, the audience, two or three venues, a cadence, and how you will know it landed |
| Executive presence | A table: situation, what you do now, the likely read, the change to run next occurrence |
| Negotiation | What to establish before naming a number, three ways to reason about ranges, a six-beat script skeleton, response handling, the written ask |
| Pivot path | Transferable-skill map, bridge roles, proof you still need sorted by time, friction points you can and cannot absorb |
| Network map | Roles to reach by function, the ask per contact, warm or cold state, next dates |
| Interview prep | Likely questions with what each tests and the evidence slot for your answer, for the rooms you are in now: promotion panel, internal move, skip-level. A pack written against a job description you are applying to is `applicant-kit`'s |
| The plan | `career-plan.md`: position, target, obstacle, evidence, case, ask, network, actions this week, dated milestones, gaps |

`tests/test-prompts.md` holds the trigger cases, including the near-misses this skill must hand away.

## Not for

Application documents. Resume and CV rewriting, the LinkedIn headline and About rewrite and the cover letter system belong to the installed `applicant-kit`; judging a document (first-impression scan, ATS check, rejection reasons, gap analysis, a LinkedIn profile audit, "why no callbacks") belongs to the installed `recruiter-lens`. Searching, shortlisting, tracking and following up on live roles belongs to the installed `application-pilot`, and learning a skill from scratch (study plan, practice routine, how long it takes) belongs to `study-system`. career-track does those handoffs instead of half-doing them: it routes with a filled handoff block, and its positioning line, evidence base and gap list are what those skills need as input. It also will not invent metrics, quote a market salary range without a dated source, tell you what a named company pays or promotes, or promise that a promotion, raise or offer follows.

## Install

```
npx skills add arm-pz/career-track --skill career-track
```

Or copy `skills/career-track/` into your agent's skills directory (`.claude/skills/`, `.agents/skills/`, `.cursor/skills/` or `.qoder/skills/`). With Claude Code plugins, `.claude-plugin/plugin.json` makes the repo installable as a plugin; add it to your marketplace repo as an entry pointing at `arm-pz/career-track`.

## Structure

```
career-track/
├── README.md
├── LICENSE
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── career-track/
│       ├── SKILL.md                 # intake, modes, output shape, quality bar, handoffs
│       └── references/
│           ├── planning.md          # positioning, promotion, review, pivot, network, presence
│           └── negotiation.md       # before the number, ranges, script skeleton, responses
└── tests/
    └── test-prompts.md
```

## Credits

The scope list comes from a public "replace ChatGPT" prompt thread circulating on X in October 2026 (the Career Accelerator prompt in that thread). Its persona framing and its outcome promises are not carried over; the working contract, the honesty rules and the sibling boundaries are this repo's.
