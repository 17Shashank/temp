# temp
# SPEAKER SCRIPT
## Synthetic Monitoring for Markets Applications
### 5 minutes · 4 speakers · 6 slides

---

## THE STORY IN ONE PARAGRAPH

Before every trading day, someone has to confirm our critical applications actually work. That work never finishes, and the list only grows. We automated it across twelve Markets applications and removed 116.75 hours of manual effort every month. More than that, every run now writes its own evidence, so when something does break, support starts with facts instead of questions.

---

## THE NARRATIVE ARC

Each slide answers a different question. Nothing repeats.

| Slide | Question | Beat | Speaker | Time |
|---|---|---|---|---|
| 1 | Who are we | Opening | 1 | 15s |
| 2 | Why does this need solving | The work never finishes | 1 | 58s |
| 3 | What did we change | The two mornings | 2 | 98s |
| 4 | What did it deliver | The numbers | 3 | 80s |
| 5 | Where exactly | The receipts | 4 | 35s |
| 6 | Close | Understatement | 4 | 10s |

Total 296s. **Rehearse to 4:30. Spoken delivery always runs long.**

**Division of labour:** slide 2 carries the argument, slide 3 carries the story. Slide 2 stays abstract because the flowchart is not on screen yet. Every concrete detail of the manual process, the KB document, the five o'clock start, the screenshot, the escalation, belongs to slide 3 where the audience can see it.

---

# SPEAKER 1 · COVER AND SLIDE 2
### Target 73 seconds

**[COVER, 15s]**

> Good morning. We are from GTSM Markets RTB Automation, and over the past eight weeks we have been working on synthetic monitoring for Markets applications.
>
> I want to start with something that happens every single morning, in every bank, before any of us are watching the market.

*Pause. Advance.*

**[SLIDE 2, 58s]**

> Every trading day, before any desk starts trading, someone has to confirm our critical applications are actually working. Not that the servers are on, but that a trader can log in, see their positions, get a live price, and place an order.
>
> Across Markets, that is dozens of checks, every single day, on a deadline that never moves.
>
> **[BEAT. Slow down.]**
>
> In site reliability engineering there is a word for that kind of work. It is called toil. Work that has to be done, has to be done exactly right, and has to be done again tomorrow no matter how well it went today.
>
> It is not that the work is unimportant. It is that it never finishes. And the list only ever gets longer, while the window before the market opens stays exactly the same length.
>
> **[Gesture to the navy band.]**
>
> Synthetic monitoring is how you take that pressure off. Automated monitoring of critical business journeys, validating application health, availability and functionality, before business users are impacted.
>
> A machine runs the same check the same way at five in the morning as it does at five in the evening. It never gets pulled onto something more urgent. And it writes down exactly what it saw, every single time.
>
> The routine execution moves to a machine. The judgement stays with the team.
>
> Start of day. Start of week. End of day. Those are the checks we automated.
>
> **So let me show you what that actually looks like, today and now.**

**Delivery notes**
- **Toil** is the hook. Say it, then hold one full second of silence.
- *"It is not that the work is unimportant. It is that it never finishes."* is the emotional centre. Say it plainly, with no added emphasis, and let it land on its own.
- *"The routine execution moves to a machine. The judgement stays with the team."* is your insurance on the jobs question. Deliver it once, clearly, and never return to it.
- Do not describe the KB document, the screenshot or the escalation here. That is slide 3's material and describing it twice kills the flowchart.
- The final line is the handoff. Do not soften it into a question.

---

# SPEAKER 2 · SLIDE 3
### Target 98 seconds. The longest section.

**[SLIDE 3, manual rail. Walk the nodes as you speak.]**

> This is the manual flow today.
>
> Depending on the region, an analyst starts at five in the morning, or is still going at midday. They open the KB document, which lists every check for that application. They work through them by hand, screen by screen. They record what they find. They send the results out on email or Teams. And if something failed, they screenshot it and escalate to L2.
>
> **[BEAT.]**
>
> And that is where it gets slow. Because L2 opens that email and starts asking questions. What exactly did you see. What time did it happen. Can you get back in and reproduce it. Was anything else failing at the same time.
>
> None of those are unreasonable questions. But every one of them costs minutes, and every one of them is being asked while the clock runs towards the open. The information existed. It was on someone's screen forty minutes ago. It was just never captured in a form anyone else could use.
>
> **[Move to the automated rail.]**
>
> Here is what we built instead. Web applications automated in Playwright. Desktop applications in UiPath, on the PACE RE framework. Each one developed, tested, and scheduled in Autosys so it fires at the exact time the check is due, on the same schedule the team works to today.
>
> And every single run writes its own evidence. Logs, JSON, CSV, screenshots. That lands on a shared drive, and ITRS Geneos reads it directly.
>
> **[BEAT. This is the payoff of the slide.]**
>
> So that same failure now surfaces on a monitoring dashboard, before anybody has logged in. And when L2 picks it up, they are not starting with questions. The logs are there. The screenshots are there. Timestamped, from the exact moment the check ran.
>
> The investigation starts where it used to start forty minutes in.
>
> **[Framework qualities. Brisk, three short sentences.]**
>
> And it holds up. It is production ready, because PACE RE gives us retries and exception handling, so a slow application does not raise a false alarm. It is scalable, because a new application plugs into the same structure rather than starting from scratch. And it is maintainable, because it is documented and handed over, not sitting on one person's machine.

**Delivery notes**
- Walk the manual rail physically. Point at each node as you name it. The audience should be reading the flowchart with you.
- The four L2 questions go quickly, one after another, no pause between them. The pile-up is the point.
- *"None of those are unreasonable questions"* protects everyone in the room. Say it warmly and mean it.
- Land hard on *"Timestamped, from the exact moment the check ran."*
- *"The investigation starts where it used to start forty minutes in"* is the strongest business line in the deck. Pause before it. Pause after it.
- The three framework qualities are brisk. Do not elaborate on any of them. **If the presentation is running long, this is the first place to cut.**

**Handoff:** *"So what did that add up to?"*

---

# SPEAKER 3 · SLIDE 4
### Target 80 seconds

**[SLIDE 4]**

> Over eight weeks, across twelve applications, we removed a hundred and sixteen point seven five hours of manual effort every month.
>
> **[BEAT. Let it sit. Do not explain it yet.]**
>
> That is not time saved by going faster. That is work that used to need a person, every day, before the open, and now does not need one at all.
>
> Behind that number are five hundred and thirty five functional touchpoints automated, across three business lines.
>
> **[Move to the chart.]**
>
> In Equities, that is EQ-SDM, Tapas3, JSDA iMatch, BATMAN and Message Search. Around fifty hours a month.
>
> In Prime and Repo, XGEN and IREPO. Thirty hours.
>
> In Securitized Products, LION, SPOne, SP-CATS and Spectra. Thirty seven hours, across the largest touchpoint count of the three, because those are big desktop applications with a lot of screens to validate.
>
> **[BEAT. Business impact moment. Slow right down.]**
>
> And I want to put that in context. This is twelve applications, in one part of one division. GTSM Markets supports many more than twelve. Every RTB team in this bank is running some version of the same daily checks, by hand, this morning.
>
> If the framework we built is applied across even a fraction of them, the hours we are describing here are the smallest version of this number that will ever be true.

**Delivery notes**
- Say **116.75** precisely. The decimal signals measured, not estimated.
- *"That is not time saved by going faster"* pre-empts the obvious challenge and buys credibility for everything after it.
- The final two paragraphs are the business impact award. Do not rush them, do not smile through them, and add nothing after them.

**Handoff:** *"Those are the totals. Here is where every one of them comes from."*

---

# SPEAKER 4 · SLIDE 5 AND CLOSE
### Target 45 seconds

**[SLIDE 5, the table]**

> This is every application. The business it supports, the tool, the touchpoints, how often it runs, and the manual effort saved each month.
>
> I will leave it up rather than read it. The row that matters is the total. Twelve applications. Five hundred and thirty five functional touchpoints. A hundred and sixteen point seven five hours a month.
>
> **[BEAT.]**
>
> Eight weeks ago, every one of these checks was somebody's morning.
>
> Now every one of them runs before business users are impacted.
>
> **[Advance to thank you.]**
>
> Thank you.

**Delivery notes**
- Do not read the table. Gesture at it, name the total row, stop.
- *"Eight weeks ago, every one of these checks was somebody's morning"* is the emotional close. Pause before it. Pause after it.
- The final line is the exact phrase from the definition on slide 2. That is deliberate. Deliver it slowly, then stop talking. No "any questions", no "we hope you found this useful". Just thank you.

---

## THE FIVE MOMENTS THAT WIN THE AWARDS

If anything gets cut for time, protect these.

**1. "It is not that the work is unimportant. It is that it never finishes."**
Defines toil in plain English and respects the people doing it. Storyteller.

**2. "The information existed. It was on someone's screen forty minutes ago. It was just never captured in a form anyone else could use."**
Names the real failure without blaming a person. Storyteller.

**3. "The investigation starts where it used to start forty minutes in."**
The most useful sentence in the deck for anyone who has run a bridge call. Business impact.

**4. "The hours we are describing here are the smallest version of this number that will ever be true."**
Extrapolates twelve applications to the whole bank without inventing a figure. Business impact.

**5. "Eight weeks ago, every one of these checks was somebody's morning."**
Human, understated, lands the whole story in twelve words. Storyteller.

---

## THE SEVEN PAUSES

The beats matter as much as the words. In order:

1. After **toil**, one full second
2. After *"it never finishes"*
3. After the manual rail, before *"And that is where it gets slow"*
4. After the four L2 questions
5. Before *"The investigation starts where it used to start forty minutes in"*
6. After **116.75**, before explaining it
7. Before *"Eight weeks ago, every one of these checks was somebody's morning"*

---

## QUESTIONS YOU SHOULD EXPECT

**"Why is the hours bar longer than the touchpoints bar on Equities?"**
> Different units on a shared scale. Touchpoints in navy, hours in cyan. They read as two separate series, not against each other.

**"How do you know it saved 116.75 hours?"**
> It comes from the documented check durations and frequencies in the existing KB and check records, per application, per month. That is the time the checks were taking, not an estimate of how long they might take.

**"What happens when the automation itself fails?"**
> PACE RE handles retries and exception handling, so a slow application does not raise a false alarm. If a check genuinely cannot complete, that surfaces in Geneos the same way a failure would, and the fallback is the existing manual process.

**"Are you replacing the L0 and L1 teams?"**
> No. The routine execution moves to a machine. The judgement, the escalation and the decisions stay with the team. What changes is that they are not spending the first hours of the day executing checks by hand.

**"Who maintains this after you leave?"**
> The framework is documented, the code is in GTSM GitLab, and the structure is identical for every application, so a new check is an extension rather than a new build. That was a design goal, not an afterthought.

**"Is this integrated with Geneos today?"**
> The evidence and status files publish to the shared monitoring location in the format Geneos reads. Full onboarding is the next step, and the automation side of it is ready.

**"Eight weeks seems fast. How much is actually in production?"**
> Give the honest split. Completed, in progress, still POC. Do not overclaim. The numbers are strong enough without it.

---

## REHEARSAL CHECKLIST

- Time it three times. If any run exceeds 4:45, cut the three framework qualities at the end of slide 3.
- Every speaker must deliver their handoff line without looking at notes. The handoffs are what make four people sound like one presentation.
- Rehearse the seven pauses. They are as important as the words.
- Whoever presents slide 4 should practise saying 116.75 aloud until it sounds natural.
- Decide in advance who fields questions. Ideally the person who owns that slide.
- Speaker 1 must not describe the KB document, the five o'clock start, the screenshot or the escalation. All of that is slide 3's material. If it leaks into slide 2, slide 3 becomes a repeat and the flowchart loses its purpose.
-
