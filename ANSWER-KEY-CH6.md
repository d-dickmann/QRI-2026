# Chapter 6 Answer Key (Instructor Resource)

**CONFIDENTIAL — Do not share with students**

---

## Drill Questions

### Section 1: Identifying Storybook Functions

| # | Question | **Correct Answer** |
|---|----------|-------------------|
| 1 | Which is NOT a storybook function? | **ramp()** |
| 2 | osc() behavior | **repeats the same pattern over and over** |
| 3 | hillside() behavior | **starts at a low value and gradually levels off at a higher value** |
| 4 | hill() behavior | **goes up from a baseline and then back down to the baseline** |
| 5 | double() behavior | **the output doubles for every unit increase in input** |
| 6 | doublings() relationship to double() | **doublings() tells you the input needed to reach a given output from double()** |
| 7 | Daily temperature function | **osc()** |
| 8 | Technology adoption function | **hillside()** |

### Section 2: Function Properties

| # | Question | **Correct Answer** |
|---|----------|-------------------|
| A | Positive rate of change for all positive inputs? | recip(): **False**, double(): **True**, hill(): **False**, hillside(): **True**, steady(): **True** |
| B | Period of osc() | **1** |
| C | hillside() output of 0.5 at input | **0** |
| D | double(0) = ? | **1** |
| D | double(3) = ? | **8** |
| D | double(-1) = ? | **0.5** |
| E | doublings(8) = ? | **3** |
| E | doublings(1) = ? | **0** |
| E | Input to doublings() for output -2 | **0.25** |
| F | Rate of change of flat() | **0** |

### Section 3: Input and Output Transformations

| # | Question | **Correct Answer** |
|---|----------|-------------------|
| i | Dimension of q₀ in a(q - q₀) | **same dimension as q** |
| ii | Dimension of a in a(q - q₀) | **1/[q] (reciprocal of q's dimension)** |
| iii | q₀ for oil production (half-max at 1970) | **1970** |
| iv | A for output range 0-100 (natural 0-1) | **100** |
| v | B for output range 0-100 (natural 0-1) | **0** |
| vi | Units of a for miles per gallon input | **gallons per mile** |

### Section 4: Recognizing Functions from Graphs

| # | Graph Description | **Correct Answer** |
|---|-------------------|-------------------|
| I | S-curve (pnorm) | **hillside()** |
| II | Bell curve (dnorm) | **hill()** |
| III | Exponential growth (2^x) | **double()** |
| IV | Sine wave | **osc()** |
| V | 1/x curve | **recip()** |

---

## Assignment Exercises

### Exercise 1: bear-climb-mountain (Matching Functions to Scenarios)

| # | Scenario | **Correct Answer** | Reasoning |
|---|----------|-------------------|-----------|
| 1 | Fertilizer → Crop yield | **hill()** | Too little or too much fertilizer both reduce yield |
| 2 | Experience → Salary | **hillside()** | Salaries plateau at senior levels |
| 3 | Distance from house → Familiarity | **hill()** | Most familiar nearby, unfamiliar far away |
| 4 | Study hours → Exam score | **hillside()** | Diminishing returns, maximum possible score |
| 5 | Day of year → Temperature | **osc()** | Seasonal cycling |
| 6 | Advertising → Customers | **hillside()** | Market saturation |

### Exercise 2: fox-read-book (double and doublings)

| # | Question | **Correct Answer** | Calculation |
|---|----------|-------------------|-------------|
| 1 | double(5) | **32** | 2⁵ = 32 |
| 2 | Bacteria after 10 hours | **1024** | 2¹⁰ = 1024 |
| 3 | double(-2) | **0.25** | 2⁻² = 1/4 = 0.25 |
| 4 | Doublings from 1 to 64 | **6** | 2⁶ = 64 |
| 5 | Doublings from $1000 to $2000 | **1** | One doubling |
| 6 | doublings(0.5) | **-1** | 2⁻¹ = 0.5 |
| 7 | If double(x) = 32, then x = ? | **5** | 2⁵ = 32 |
| 8 | If doublings(y) = 4, then y = ? | **16** | 2⁴ = 16 |
| 9 | Relationship | **They "undo" each other** | Inverse functions |

### Exercise 3: owl-watch-sunset (osc and periodic modeling)

| # | Question | **Correct Answer** | Reasoning |
|---|----------|-------------------|-----------|
| 1 | First zero after t=0 | **0.5** | Half period |
| 2 | First maximum | **0.25** | Quarter period |
| 3 | Cycles from 0 to 3 | **3** | Period = 1 |
| 4 | Average temp (30°F to 80°F) | **55** | (30+80)/2 = 55 |
| 5 | Amplitude | **25** | (80-30)/2 = 25 |
| 6 | Value of a for 365-day period | **1/365** | a × 365 = 1 |
| 7 | Complete temperature model | **55 + 25 × osc(day/365)** | Midline + amplitude × osc(scaled input) |

### Exercise 4: rabbit-plant-garden (Input/Output Transformations)

| # | Question | **Correct Answer** | Reasoning |
|---|----------|-------------------|-----------|
| 1 | q₀ (half-max at week 10) | **10** | hillside(0) = 0.5 |
| 2 | a (near max at week 20) | **0.2** | 0.2 × (20-10) = 2 |
| 3 | Units of a | **per week** | Cancels weeks to give dimensionless |
| 4 | A (scale to 2 million) | **2000000** | Multiply natural 0-1 range |
| 5 | Units of A | **views** | Output units |
| 6 | B (starts at 0) | **0** | No vertical shift needed |
| 7 | Complete model | **2000000 × hillside(0.2 × (week - 10))** | Full transformation |
| 8 | Views at week 5 | **about 500,000** | hillside(-1) ≈ 0.16, × 2M ≈ 320K (closest: 500K) |

### Exercise 5: deer-cross-river (recip, double, doublings)

| # | Scenario | **Correct Answer** | Reasoning |
|---|----------|-------------------|-----------|
| 1 | Workers → Task time | **recip()** | More workers = less time (inverse) |
| 2 | Time → Savings balance | **double()** | Compound growth (exponential) |
| 3 | RAM → Perceived performance | **doublings()** | Logarithmic perception |
| 4 | Days → Infected people | **double()** | Early epidemic = exponential |
| 5 | Sound power → Perceived loudness | **doublings()** | Decibel scale is logarithmic |
| 6 | Distance → Light brightness | **recip()** | Inverse square law |
| 7 | Practice hours → Skill | **doublings()** | Diminishing returns (log curve) |

---

## Quick Reference: Storybook Functions

| Function | Formula | Shape | Key Feature |
|----------|---------|-------|-------------|
| flat() | 1 | Horizontal line | No change |
| steady() | x | Straight line | Constant rate |
| osc() | sin(2πx) | Wave | Period = 1, range [-1, 1] |
| hill() | dnorm(x) | Bell curve | Peak at x=0 |
| hillside() | pnorm(x) | S-curve | 0.5 at x=0 |
| double() | 2^x | Exponential | Output = 1 at x=0 |
| doublings() | log₂(x) | Log curve | Output = 0 at x=1 |
| recip() | 1/x | Hyperbola | Approaches 0 as x→∞ |
