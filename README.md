# **Application Processor**

A small AI-powered job search assistant built to help me find and apply to better product roles.

The goal is not to automate applications blindly. It is to turn the job-search process into a structured product workflow:

**Job → Screening → Evidence → CV → Application → Outcome → Learning**

## **Why**

Applying to jobs repeatedly involves a lot of the same work:

- Understanding a job description
- Assessing whether the role is actually a good fit
- Identifying relevant experience
- Choosing the right version of my CV
- Finding the strongest stories
- Tailoring applications
- Tracking outcomes
- Learning what positioning works

I am building a small AI system to make that process faster and more consistent without losing human judgement.

## **Current MVP**

The first version focuses on one question:

**Is this job worth applying to, and how should I position myself?**

Given a job description, the system should return:

- `APPLY`, `STRETCH` or `SKIP`
- Why
- Best CV
- Strongest matching evidence
- Relevant gaps
- Potential risks
- Recommended application angle

The final decision remains human.

## **Principles**

### **Evidence over keywords**

A job description saying “Growth” does not automatically make me a Growth PM.

A job saying “AI” does not automatically mean I have production AI experience.

The system should reason from actual evidence rather than matching keywords blindly.

### **Transferable experience ≠ direct experience**

The agent should clearly distinguish between:

- Direct experience
- Transferable experience
- Adjacent experience
- Domain expertise
- Missing experience

### **Truth over optimisation**

The goal is to make the strongest truthful case for my experience.

The system should never invent:

- Responsibilities
- Metrics
- Domain expertise
- Technical experience
- Product ownership
- Seniority

## **Project structure**

```text
application-processor/
│
├── app/
│   ├── agent.md
│   ├── main.py
│   └── product-mvp.md
│
├── cover_letters/
│
├── cvs/
│
├── knowledge/
│   ├── applications.md
│   ├── cv-library.md
│   ├── dogfood-jds.md
│   ├── preferences.md
│   ├── profile.md
│   ├── skills.md
│   └── stories.md
│
├── prompts/
│   ├── screening.md
│   ├── tone.md
│   └── write-application.md
│
├── .gitignore
├── README.md
└── requirements.txt
```

## **Knowledge**

The `knowledge/` folder contains the information the system uses to reason about me.

- `profile.md` — professional identity, strengths and working style
- `preferences.md` — preferred roles, companies and working environments
- `stories.md` — concrete career stories and evidence
- `skills.md` — structured skills and technical capabilities
- `cv-library.md` — CV selection and positioning rules
- `applications.md` — application history and outcomes
- `dogfood-jds.md` — previously evaluated jobs used as a test set

The CV and cover letter PDFs remain the source material for the actual application documents.

## **Prompts**

The `prompts/` folder contains the behavioural instructions used by the system.

- `screening.md` — evaluate a job
- `write-application.md` — prepare application material
- `tone.md` — maintain a consistent writing style

## **Development approach**

This project is intentionally starting small.

The first version is not an autonomous application bot.

The initial workflow is:

```text
Paste job description
        ↓
     Screen
        ↓
Select CV
        ↓
Identify evidence + gaps
        ↓
Human decision
```

Only after this works reliably will additional capabilities be added.

## **Dogfooding**

Previously evaluated job descriptions are stored in `knowledge/dogfood-jds.md`.

These provide a small benchmark for testing whether the agent reaches sensible decisions based on the same information a human would use.

The aim is to improve the system through real application outcomes rather than building unnecessary complexity upfront.

## **Roadmap**

### **MVP**

- Profile
- Preferences
- Career stories
- CV library
- Skills library
- Screening agent
- CV selection
- Test against previous jobs

### **Next**

- Job URL ingestion
- Application writing
- Application tracking
- Interview preparation
- Outcome analysis
- Learn which positioning generates interviews

### **Later**

- Job discovery
- Automated application preparation
- Optional browser automation

## **Status**

Early prototype.

The project is being developed through real job applications and iterated based on what actually helps.