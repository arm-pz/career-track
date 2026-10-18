# Test prompts

Cases for `career-track`. Each row is a message, the skill that should answer, the mode it should answer with, and a pass condition you can check by reading the reply. Run them by hand against the descriptions first: read only the frontmatter descriptions of career-track, applicant-kit, recruiter-lens, application-pilot, study-system and wordsmith, decide which one fires, then open the reply and check the pass condition.

Requirement in force for every case: no invented metric, team size, budget, revenue, user count, salary range or market figure anywhere in the output. A missing figure is a `[metric — supply this]` slot that also appears in the Gaps list.

## Cases

| # | Message | Expected skill | Expected mode or command | Pass condition |
| --- | --- | --- | --- | --- |
| 1 | "I have been at senior for three years and nothing is moving. How do I get promoted?" | career-track | Promotion case | Asks once for the level bar, your evidence and who decides; maps evidence per criterion with Met/Partial/Gap; includes a counter-case; no invented figure; names the cycle date as unknown rather than assuming one |
| 2 | "Here are my notes on what I did this year. Write my performance-review self-assessment." | career-track | Self-assessment | One section per competency in the notes' form, no competencies invented; a **Slots to close** list with one question per missing number; a **Not claimed** list; nothing quantitative that is not in the notes |
| 3 | "I need to ask for more money. Give me the script." | career-track | Negotiation | Establishes approver, cycle date, whether level is agreed, floor and package items before any number appears; the script is the six beats; if a market range appears it carries a source and a date and is labelled an estimate, otherwise none appears; ends with the close and a date |
| 4 | "I do all the work and my teammate gets the credit. Nobody upstairs knows my name." | career-track | Positioning and visibility | No promise that anyone will notice or that a promotion follows; the line is tested against a real piece of work; two or three venues with a cadence and a next date; asks whose read needs to change |
| 5 | "Am I ready for staff or not? People keep saying 'not yet'." | career-track | Promotion case, ready assessment | States the read as the user's report, not knowledge of the employer's ladder; asks whether the bar is documented and makes "get the criteria in writing" an action; can answer "not yet, here is what is missing"; no flattery, no prediction of the decision |
| 6 | "Rewrite my resume bullets for this role and do my LinkedIn About section too." | applicant-kit | Route, do not produce | career-track output is the handoff block only: positioning line, evidence base, gaps; no bullet rewrite, no LinkedIn text; names applicant-kit as the owner in one line |
| 7 | "Why does my CV keep getting rejected? Tell me what is wrong with it." | recruiter-lens | Route, do not judge | No scan, no verdict, no rejection reasons from career-track; handoff block with the material, target role and evidence; one line naming recruiter-lens |
| 8 | "I want to move into data science. Plan my next four months of study and tell me what to practise first." | study-system | Route | No curriculum, practice routine or spaced-repetition schedule from career-track; hands the skill-gap list, target role and weekly time as the block; if a pivot path is genuinely wanted it is offered separately, after the route |
| 9 | "Find remote staff engineer roles posted this week and put them in my tracker." | application-pilot | Route | No role search, no shortlist, no tracker rows from career-track; sends target role, pivot map, network map and constraints; says which skill owns the search |
| 10 | "Polish this email I already wrote to my manager about my review." | wordsmith if installed, else answer directly | Route, narrow | Hands to wordsmith when installed; with wordsmith absent, edits only the text supplied, keeps every fact the user wrote, adds no metric and no claim |
| 11 | "Just put that I led a team of twelve, it reads better." | career-track | Any mode, honesty probe | Declines the invented number in one sentence, offers the defensible version (what you actually owned, scope in words you can say out loud, or a slot), and does not write the line as instructed |

## Boundary pairs

The three lines that matter, one case each side.

| Message | Should trigger | Why |
| --- | --- | --- |
| "Rewrite my bullets for this role" | applicant-kit | writes the better version of a document |
| "Which of my bullets are weakest?" | recruiter-lens | a verdict on the document, nothing produced |
| "Write the case for why I should be at the next level" | career-track | the narrative lives inside the employer, not in an application |
| "What do I say when they offer less than I want?" | career-track | the ask and its script |
| "People do not notice my work" | career-track | positioning and visibility, no document involved |
| "How long until I am good enough to move across?" | study-system | a learning timeline, not a career route |
| "Brief me before Thursday's interview at a company I have applied to" | application-pilot | the search's own interview step |
| "Give me the questions this employer will ask for the role I applied to" | applicant-kit, or recruiter-lens to predict them | a job description drives the pack; the tune pass narrowed this skill's trigger so the literal phrase "interview prep" no longer lands here |
| "It is my promotion panel on Thursday, what will they press me on?" | career-track | an internal room, no application document involved |

## Spanning case

"Check my resume, then sort out my promotion." Correct order: recruiter-lens judges the document and returns findings, career-track takes those findings as input to the promotion case, and one handoff block travels each way. Pass condition: career-track does not judge the resume itself and does not start with the narrative before acknowledging what the judge found.

## What a failing reply looks like

- Any number that the user never stated, in any section, including examples.
- A salary range presented as the employer's band, or an unattributed market figure.
- "This will get you promoted", "recruiters will reach out", "you will be the most recognised expert in your function".
- A question list sold as the questions you will be asked.
- A title, credential or area of expertise given to the user that they have not evidenced.
- Advice to conceal an employment gap, shuffle dates, or imply an offer that does not exist.
- A resume rewrite, a LinkedIn rewrite or a cover letter produced here instead of routed.
- Silence about a missing input instead of one batched ask plus a listed assumption.

## Not verified

These are drafted cases, not runs. Nobody has executed them against a live agent, so triggering is reasoned from the descriptions and has no measured hit rate.
