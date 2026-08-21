# tekmir-challenge

## Track Chosen

Track A, the SignalDesk domain packet.

## What I Built

A short notebook that answers one question: did the Aug 4 prompt change help, hurt, or just make things harder to read? It cleans the export, compares before and after rates per workflow, charts acceptance rate by day, and ends with a plain-English verdict and a suggested weekly health check.

## Who It Is For

The SignalDesk product team, specifically whoever has to decide whether to roll the new prompts out more widely. It should be readable without opening the code.

## Data Or Source Used

`sample-data/product_usage_events.csv` from the challenge repo. 41 rows, 7 days, 3 workflows. The notebook loads it straight from the raw GitHub URL so it runs anywhere.

## Assumptions I Made

- Aug 4 is the change date for all three workflows, based on the notes column.
- Rows with "traffic spike from demo account" and "duplicate export row" are not real usage and were dropped.
- Reply draft on Aug 7 was excluded from the before/after comparison because the review policy changed that day, so it doesn't measure the prompt on its own.
- Rates are pooled (sum counts first, then divide) rather than averaged per row, so small-sample days don't get the same weight as busy days.

## Data Issues Or Caveats I Noticed

- "product" vs "Product" casing in the team column.
- One exact duplicate row.
- One missing user_rating, one missing median_confidence.
- "small sample" days on Aug 1 for Feedback clustering.
- Two changes (prompt and review policy) landed three days apart, which makes Reply draft hard to read.
- Only three clean days on each side of the change. Nothing here is statistically strong.

## What I Would Do Next With More Time

Ask the Support reviewers whether the Aug 7 flag spike was worse output or stricter rules. Add a second quality signal, since "accepted" can just mean "easier to fix than regenerate." Look at whether the prompt change behaved differently by source (manual vs email vs queue).
