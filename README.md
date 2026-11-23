# Handoff Check

**Live demo:** https://handoff-check.netlify.app
**Built by:** Sadé Bobb · SMJB Implementation Group · Introduction to NLP (CAI2300C), Dr. Ernesto Lee, Miami Dade College

Paste a proposal, scope of work or sales-call notes. Handoff Check uses natural language processing to pull out deliverables, deadlines, owners, money and vague scope language, scores how ready the deal is to hand to delivery, and builds a kickoff checklist.

## Ideal client profile (ICP)

- **Company:** marketing, digital, SEO, web, creative and CRM/RevOps agencies first, then consultancies and professional-services firms; about 8–50 people; several client projects at once; work split across a CRM, a project tool, email and Slack.
- **Buyer:** founder/CEO, COO or head of operations, or the client-services lead who owns onboarding.
- **Pain:** what sales promised isn't what delivery hears; dates and owners get lost between proposal and kickoff; vague scope turns into scope creep.
- **Success:** every signed deal reaches delivery with deliverables, dates and owners named, and scope risks caught before kickoff.

## NLP pipeline (clean → tokenize → represent → model → evaluate)

1. **Clean:** normalize whitespace and quotes.
2. **Tokenize:** split into sentences and lowercase word tokens.
3. **Represent:** stopword removal, light stemming, TF-IDF across sentences for key topics.
4. **Extract:** commitment-verb detection for deliverables, regex patterns for dates and money, role and name detection for owners, a vague-scope lexicon for risks, and a small sentiment lexicon for tone.
5. **Score:** a 0–100 readiness score from what is present (deliverables, owners, dates, price, sign-off) minus penalties for flagged risks.

Everything runs in the browser in plain JavaScript. No text leaves the page and no API keys are needed.

## Run locally

Open `index.html` in a browser. There is no build step.

## Note

This is a class demo, not legal or contract advice.
