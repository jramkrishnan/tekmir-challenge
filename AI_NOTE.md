# AI Collaboration Note

## Did You Use AI?

Yes. Claude, throughout.

## How You Used It

I used it the way I'd use a senior colleague sitting next to me. I ran the code myself in Colab and pasted outputs back, and it helped me structure the steps (sanity checks, clean, label before/after, compare, chart, verdict) and wrote the first draft of the matplotlib code. When I wasn't sure what a pandas call was doing, I asked and it explained.

## One Prompt, Workflow, Or Moment That Helped

The most useful moment was asking it to explain why averaging per-row rates can be misleading. It showed me that a 5-session day gets the same weight as a 100-session day when you average rates directly, and that summing the counts first then dividing (pooling) is the right approach when sample sizes vary. That changed how I built the before/after comparison table.

## One Thing You Verified Or Decided Yourself

I read every row in the notes column myself before writing any analysis code. That's where the Aug 4 change date, the demo account spike, the duplicate export row, and the Aug 7 policy change all came from.

The biggest call I made was removing Reply draft on Aug 7 from the before/after comparison. The note said "review policy changed mid-day," so that day's flag spike and acceptance drop could be the policy, the prompt, or both. Leaving it in made it look like the prompt hurt Reply draft. Taking it out showed Reply draft was actually flat or slightly better. AI can compute the rates either way, but it can't decide which rows belong in the comparison. That was my call, and it changed the whole verdict.

I also chose to chart only acceptance rate. Completion was flat everywhere and I'd already decided flag rate couldn't be trusted, so plotting it as if it meant something would have contradicted my own conclusion.
