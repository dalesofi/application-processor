/job-agent
  /candidate
    profile.md
    cv-library.md
    stories.md
    skills.md
    preferences.md



JD parser

Give the agent a JD. Have it extract:

{
  "role": "",
  "company": "",
  "location": "",
  "salary": "",
  "seniority": "",
  "domain": "",
  "must_have": [],
  "nice_to_have": [],
  "responsibilities": [],
  "signals": [],
  "red_flags": []
}

then build a reccomender to prioritize the jds to apply 

Requirement:
B2B SaaS experience

Evidence:
Ironhack B2B product engine
CVSD26-E
11+ international markets

Strength: STRONG

Requirement:
Marketplace ranking

Evidence:
No direct ownership found.

Strength: GAP



**Add CV selection**



This becomes a simple classification problem.

AI / GenAI → 8-26
B2B / SaaS / platform → CVSD26-E
Growth / UX / digital → CVSD926-Z
Data / web / marketplace → cvsd26-r
Product Ops / Program → JJ
Commercial B2B → CVSD26

I chose CVSD926-Z because 5 of the 7 core requirements map directly to its positioning.”



That explanation is important.

**STEP 5 — Add an “application decision”**

### **APPLY**

Strong enough fit and worth your time.

### **STRETCH**

Real gaps, but strategically interesting.

### **SKIP**

Too many hard requirements missing.

**STEP 6 — Generate the application package**

Only *after* the previous steps.

The agent gets:

- JD
- selected CV
- relevant evidence
- company information
- your preferred tone

output: 

APPLICATION STRATEGY

CV:
CVSD926-Z

Positioning:
...

Strongest evidence:
1. ...
2. ...
3. ...

Gaps:
...

Potential concern:
...

Cover letter:
...

Likely application questions:
Q1...
Answer...

Q2...
Answer...

**STEP 7 — Add salary reasoning**

Inputs:

- published range
- location
- seniority
- market data
- your experience
- your minimum target

Published: €66–108k
Suggested ask: €95k
Target: €90–100k
Reason: ...