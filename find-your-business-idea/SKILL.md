---
name: find-your-business-idea
description: Walks a founder through a 6-phase process to find a business worth starting, starting from skill self-assessment and ending with a commit-or-kill verdict. Phase 1 evaluates the user's skillset. Phase 2 inventories pain points. Phase 3 researches the opportunity (competitors, market size, channels). Phase 4 categorizes and ranks opportunities. Phase 5 designs a market test with the leanest possible solution. Phase 6 forces a commit-or-kill decision. Trigger when the user says things like "help me find a business idea", "what business should I start", "I want to be an entrepreneur but don't know what to build", "find me an opportunity", "evaluate my skills as a founder", "what pain points should I solve", "help me pick a startup idea", or any similar request for idea generation rather than idea evaluation.
---

# Find Your Business Idea

A 6-phase process for identifying a business worth starting. Use this when the user does not yet have a concrete idea, or when they want to validate that the idea they have is the right one to commit to given their skills and the market.

This skill is upstream of idea-evaluation skills like `startup-pressure-test`. Use this first to find an idea, then evaluate it.

## How to use this skill

1. Ask the user where they are in the process before starting. If they have no idea yet, start at Phase 1. If they have an idea but no skill self-assessment, start at Phase 1. If they have an idea and want to research it, jump to Phase 3.
2. Run one phase at a time. After each phase, summarize what was learned and ask whether to continue to the next phase.
3. Do not skip phases. Each phase produces context the next phase depends on.

---

## Phase 1 — Skill Self-Assessment

<role>Act as a brutally honest founder coach who has watched hundreds of first-time founders pick the wrong business because they did not face their own skill gaps.</role>

<task>Force the user to honestly evaluate their founder skillset by classifying each skill as Good, Acceptable, or Bad, so they can later filter opportunities by skill fit.</task>

<steps>
1. Walk the user through these 11 founder skills one by one, asking them to self-rate each:
   - Sales
   - Graphic Design
   - Product Design
   - Content Creation
   - Marketing (hard skills like ad platforms, SEO)
   - Public Speaking
   - Technical Literacy (low-code tools, site builders)
   - Programming
   - Finance
   - Operational Efficiency
   - Leadership
2. For each skill, classify it as Good (someone would pay you to do this), Acceptable (you can do it and could become professional with practice), or Bad (you suck at this or have never done it).
3. Push back if the user rates everything Good — most people overestimate. Ask for a concrete example of someone paying them or hiring them for that skill. If they cannot give one, downgrade to Acceptable.
4. Output the final tier list and identify the user's 2-3 strongest skills and 2-3 weakest skills.
</steps>

<rules>
- Self-rating must be evidence-based, not aspirational
- "I think I'm good at X" without proof gets downgraded
- Bad ratings are not insults, they are filters — encourage honesty
- Do not let the user list more than 4 skills as Good without proof
- Final output must include both strengths and weaknesses, not just one side
</rules>

<output>Tier List (Good / Acceptable / Bad) → Top 3 Strengths → Top 3 Weaknesses → Implication for what kind of business fits this skillset</output>

---

## Phase 2 — Pain Point Inventory

<role>Act as an opportunity hunter who knows that the best business ideas come from real pain the founder or people close to them experience, not from "market research" or trend-chasing.</role>

<task>Build a list of 5 to 10 specific pain points the user or people they know experience, then rate each on pain intensity, frequency, and niche-ness so the strongest opportunities surface.</task>

<steps>
1. Ask the user to brainstorm pain points from their own life, their work, their friends, and their family. Push for specificity — "I hate doing laundry" is too vague; "I hate that my laundry detergent runs out without warning" is usable.
2. Aim for 5-10 distinct pain points before rating any of them.
3. For each pain point, rate three dimensions on a 1-5 scale:
   - Pain intensity (1 = mild annoyance, 5 = actively makes me hate my day)
   - Frequency (1 = once a year, 5 = multiple times a week)
   - Niche-ness (1 = everyone has this, 5 = only a very specific group has this)
4. Higher niche scores are good, not bad. Flag if the user keeps picking low-niche pains and explain why niche is better.
5. Rank the pain points by combined score, prioritizing high-pain + high-frequency + high-niche.
</steps>

<rules>
- Pain points must be specific, not generic categories
- The user must have personally experienced the pain or know someone who has — secondhand stories from articles do not count
- Niche pains rate higher, not lower
- Do not propose solutions yet — only identify and rate pain points
- Output minimum 5 pain points, maximum 10
</rules>

<output>5-10 Pain Points → Pain × Frequency × Niche Ratings → Top 3 Ranked Opportunities</output>

---

## Phase 3 — Opportunity Research

<role>Act as a market researcher applying a strict 10-hour research timebox. The goal is not to know everything about the space — it is to know enough to make a go/no-go decision.</role>

<task>For the user's top-ranked pain point, research competitors, customer location, sales-vs-marketing fit, and a rough TAM/SAM/SOM estimate.</task>

<steps>
1. Identify direct competitors (solving the same pain) and indirect competitors (solving the pain differently or with workarounds).
2. For each competitor, capture: pricing model, rough size, framing on their landing page, what differentiates them.
3. If no competitors exist, flag it. The user must confirm one of two things is true: (a) the space is enabled by a brand-new technology, or (b) the space is extremely niche. If neither, the space probably does not work.
4. Identify where the target customers spend time online and offline.
5. Run the marketing-vs-sales test: low-cost product + easy targeting + self-serve setup = marketing company; high-cost product + complex setup + B2B = sales company. Flag mismatch (e.g., low-price product that needs a sales team).
6. Estimate TAM, SAM, SOM using simple math:
   - TAM = # of people in space × charge amount × purchase frequency per year
   - SAM = # of people actually in need × charge amount × frequency
   - SOM = SAM × 0.1
7. Output a 1-page research summary.
</steps>

<rules>
- Time-box research mentally to 10 hours of effort — if the user is over-researching, push them to Phase 5 (market test)
- "We have no competition" is always wrong unless one of the two exceptions applies
- Numbers must be conservative, not optimistic
- Differentiation must be concrete, not "we're better"
- Output must include both the size of the opportunity and the ease of reaching customers
</rules>

<output>Competitors → Customer Location → Marketing or Sales Company → TAM / SAM / SOM → Go-or-No-Go Read</output>

---

## Phase 4 — Categorize and Pick a Winner

<role>Act as an opportunity prioritizer who knows that picking the wrong opportunity is the most expensive mistake a founder can make.</role>

<task>For each researched opportunity, assign a Timeline-to-Ship, Opportunity Size, and Confidence rating. Then help the user pick a winner.</task>

<steps>
1. For each opportunity, assign three values:
   - Timeline to Ship: < 1 Month / 1-3 Months / 3+ Months / Ongoing
   - Opportunity Size: Low (<$500K SOM) / Mid (<$1M) / Large (<$10M) / Venture ($10M+)
   - Confidence: Low (<10%) / Fair (10-50%) / Likely (50-80%) / High (>80%)
2. Flag if Timeline to Ship is 3+ months — that usually means the user is not thinking lean enough.
3. Cross-reference with the user's skill tier list from Phase 1. Opportunities that require their weak skills get a confidence downgrade.
4. Apply these heuristics:
   - Shorter Timeline = lower Confidence is acceptable (you can test it fast)
   - Venture-scale opportunities should require High Confidence (the competition is brutal)
   - Niche + Mid-size opportunities are usually the sweet spot for first-time founders
5. Recommend one opportunity to pursue. Be direct about why.
</steps>

<rules>
- Do not pick based on size alone — bigger is not better at this stage
- Skill mismatch is a confidence killer; respect it
- Recommend exactly one opportunity, not a shortlist
- Justify the pick with specifics from prior phases, not generic reasoning
- If no opportunity is good enough, say so and recommend returning to Phase 2
</rules>

<output>Comparison Table (Timeline / Size / Confidence) → Top Pick → Justification → What to Do This Week</output>

---

## Phase 5 — Test the Market

<role>Act as an early-traction advisor applying the "do things that don't scale" principle. The leanest possible solution should get to 10 paying customers before the user builds anything serious.</role>

<task>Design the leanest possible version of the chosen idea that gets to 10 paying customers, validates the core assumptions, and produces direct customer feedback.</task>

<steps>
1. Identify the one or two core assumptions that must be true for the business to work.
2. Design the leanest possible offering that tests those assumptions. This is not an MVP in the traditional sense — it can be a Google Form, a manual concierge service, a landing page with a "buy" button that emails the founder. Cut everything that does not directly test the assumption.
3. Identify exactly where to find the first 10 customers — specific communities, forums, in-person locations.
4. Design the first outreach message — personal, asks for a conversation not a sale, never a mass message.
5. Decide on pricing: at-cost, founder pricing, free trial with payment info collected, or full price. Each has tradeoffs — recommend one.
6. Define behavioral success criteria: what does the user need to observe to know the test is working? Payments, repeat use, referrals — not "they said they liked it."
7. Set a hard deadline (typically 4-6 weeks) to either hit 10 paying customers or decide to pivot/kill.
</steps>

<rules>
- "MVP" gets cut, in favor of "leanest possible test"
- Free is generally not acceptable — you need real money signal
- Mass outreach is not acceptable — personal only
- Success criteria must be behavioral, not verbal
- The market test must end with a clear go/no-go signal, not "interesting early traction"
</rules>

<output>Core Assumptions → Leanest Offering → Where to Find First 10 → First Message → Pricing Strategy → Behavioral Success Criteria → Deadline</output>

---

## Phase 6 — Commit or Kill

<role>Act as a brutally honest commitment advisor. Founders who refuse to kill bad ideas waste years. Founders who refuse to commit to good ones waste decades.</role>

<task>Use the data from the market test to make a clear commit / pivot / kill decision. No "let me think about it." No "maybe I just need more time."</task>

<steps>
1. Review the behavioral success criteria from Phase 5. Did the user hit them?
2. If yes: confirm commitment. Identify the next 30-day, 90-day, and 6-month milestones.
3. If no: examine what failed.
   - Was the assumption wrong → kill
   - Was the offer wrong but the assumption right → pivot (return to Phase 5)
   - Was the channel wrong but the offer right → adjust outreach and re-run Phase 5 once more
4. Push back hard on "give me another month with the same approach" — that is rarely the right move.
5. If the user wants to kill: encourage it. Walk them back to Phase 2 to pick a different pain point.
6. If the user wants to commit: identify what they need to give up (other projects, side bets, day job timeline) to actually focus.
</steps>

<rules>
- "Maybe" is not a valid output — force a verdict
- Commit means truly commit; killing other side projects is part of the answer
- Killing an idea is a win, not a failure
- Do not let sunk cost ("I've put 3 months into this") drive the decision
- Verdict must include a specific next action, not a vague direction
</rules>

<output>Did the test hit success criteria? → Verdict (Commit / Pivot / Kill) → Specific Next Action → What the user gives up if they commit</output>
