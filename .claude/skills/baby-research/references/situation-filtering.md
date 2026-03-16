# Situation-First Filtering

The most important thing the research skill does is filter findings through the user's specific situation before reporting. A Wirecutter #1 pick that doesn't fit your life is noise, not signal.

## Where to Find Constraints

**Nothing is hardcoded.** Extract all constraints at runtime from project files:

### 1. CLAUDE.md (project root)
Look for sections describing the user's profile:
- Living situation (apartment/house, rooms, dedicated nursery?)
- Transport (car, transit, walking, combination)
- Pets (species, implications for sleep surfaces and gear)
- Budget level
- Timeline (due date, current week of pregnancy)
- Partner dynamics (who researches, how decisions are made)
- Preferences (new vs used, evidence-based approach)

### 2. Target file sections
Look for these section names:
- "Our Requirements"
- "Our Situation"
- "Our Setup"
- "What Matters for Us"
- "Why It Matters for Us"

These contain topic-specific constraints that supplement the CLAUDE.md profile.

### 3. Related files
Check cross-linked files for constraints that affect the current topic:
- Car seat file mentions stroller compatibility
- Crib file references nursery/space constraints
- Feeding files reference each other

## Common Constraint Types

| Constraint | Where to look | How it filters |
|-----------|---------------|---------------|
| **Space** | CLAUDE.md ("apartment," "no nursery"), space files | Filter by dimensions, weight, fold size, storage footprint |
| **Transport** | CLAUDE.md ("transit," "car"), requirements sections | Filter by portability, one-hand fold, stair-friendliness, weight |
| **Pets** | CLAUDE.md ("2 cats"), health/sleep files | Flag sleep surface safety, gear storage, allergen considerations |
| **Budget** | CLAUDE.md ("moderate budget"), file headers | Filter by price range, flag over-budget items, note registry strategy |
| **Timeline/Season** | CLAUDE.md (due date), file headers ("buy by week X") | Filter by seasonal relevance (summer baby → mesh carriers, AC needs) |
| **Location** | CLAUDE.md ("urban/suburban") | Filter by terrain needs, transit access, local resources |
| **Safety preferences** | CLAUDE.md ("new for safety-critical"), file headers | Flag used vs new guidance per item category |

## How to Apply Filtering

### Step 1: Build the filter
After reading CLAUDE.md and the target file, state the active constraints in a mental checklist:
```
Active constraints for this research:
- Apartment (limited storage, no nursery)
- Transit + car (need portability AND trunk fit)
- 2 cats (sleep surface safety)
- Moderate budget (~$X range for this category)
- July baby (summer heat affects gear choices)
```

### Step 2: Evaluate each option against constraints
For every product, recommendation, or option you find:
- Does it fit the space constraints?
- Is it portable enough for the transport mode?
- Are there pet-related safety considerations?
- Is it within budget? If over, is there a clear reason to stretch?
- Does the season affect this choice?

### Step 3: Rate Situation Fit
Add a **Situation Fit** column to every comparison table:

| Rating | Meaning |
|--------|---------|
| **Excellent** | Fits all active constraints well |
| **Good** | Fits most constraints; minor compromises noted |
| **Fair** | Fits some constraints; notable trade-offs |
| **Poor** | Doesn't fit key constraints; include only if it's a dominant market option worth explaining why it doesn't work |

### Step 4: Rank by fit, not by generic score
The table should be ordered by Situation Fit, with the best-fitting options first. If a 4.2-rated product fits perfectly and a 4.8-rated product doesn't fit, the 4.2 goes first.

## Bad vs Good Output

### Bad: Just reporting Wirecutter rankings

```markdown
## Top Infant Car Seats

1. **UPPAbaby Mesa V2** — Wirecutter's top pick. $400. Excellent safety ratings.
2. **Chicco KeyFit 35** — Budget pick. $220. Easy to install.
3. **Nuna PIPA rx** — Upgrade pick. $470. Lightweight.

Sources: Wirecutter, Consumer Reports
```

Problems:
- Ranked by review site's generic order, not by user's situation
- No situation filtering — doesn't mention transit weight, apartment storage, budget fit
- No Situation Fit column
- "Excellent safety ratings" implies price = safety (see Oster framework)

### Good: Ranked by situation fit

```markdown
## Options to Research

| Model | Type | Weight (carrier) | Price | Stroller Compat. | Situation Fit |
|-------|------|-------------------|-------|-------------------|---------------|
| **Chicco KeyFit 35** | Infant carrier | 9.6 lb | ~$220 | Extensive (adapters for most brands) | **Good** — affordable, moderate weight for transit, broad stroller compat. |
| **Graco SnugRide 35 Lite Elite** | Infant carrier | 7.5 lb | ~$170 | Broad (adapters available) | **Good** — lightest mainstream option, best value, great for transit stairs |
| **Nuna PIPA lite r** | Infant carrier | 5.5 lb (baseless: 3.3 lb) | ~$400 | Good (Nuna + adapters) | **Excellent fit, over budget** — lightest available, baseless transit mode; $400 is a stretch |
| **UPPAbaby Mesa V2** | Infant carrier | 10.1 lb | ~$400 | Best with UPPAbaby strollers | **Fair** — excellent product but heavy for transit and over moderate budget |
| **UPPAbaby Mesa Max** | Infant carrier | 12.5 lb | ~$520 | Best with UPPAbaby | **Poor** — too heavy for transit, well over budget |

> **Our situation:** Apartment + transit + moderate budget points toward the Chicco KeyFit 35 (best balance) or Graco SnugRide 35 Lite Elite (lightest for transit). The Nuna PIPA lite r is the dream pick for transit but stretches the budget — strong registry candidate.
```

Why this is better:
- Ordered by situation fit, not generic ranking
- Situation Fit column with specific reasoning
- Budget explicitly addressed (not just price listed)
- Transit weight highlighted (the key constraint for this user)
- Over-budget items included but flagged honestly
- "Our situation" blockquote synthesizes the recommendation
- Heavy/poor-fit items included but at the bottom with clear explanation

## When No Option Perfectly Fits

This happens often. When it does:

1. Present the least-bad options first
2. Be explicit about what compromises each option requires
3. Identify which constraint to relax: "If budget can stretch $50, the X becomes the clear winner. If weight is non-negotiable, the Y is the pick despite costing more."
4. Frame it as a discussion prompt: "> For partner discussion: Do we prioritize staying under $X or getting the lighter option for transit?"

## Handling Missing Constraints

If CLAUDE.md or the target file doesn't specify a constraint you'd normally filter by:

- **Don't assume.** Don't invent constraints that aren't stated.
- **Note the gap:** "No car model specified — verify fit before purchasing"
- **Present options across the range** rather than filtering too aggressively
- **Suggest the user add the constraint:** "Consider adding your car model to the Our Requirements section for better filtering"
