---
framework_version: 1.0.0
---

# Interview Preparation Guide

<!-- SETUP: STAR examples are personalized by running /setup based on your actual experience -->

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

<!-- These are populated by /setup from your actual experience. Below are templates showing the format. -->

### 1. Geosteering Guide (well-log integration, drill-well support)
**S:** Horizontal-well decisions need logs, cuttings, trajectories, and a formation surface in the same frame. Vendor files (Petrel LAS, surveys, CPS3 grids) do not line up by default.
**T:** Build a usable decision-support loop for analogue Cooper Basin Stimpee wells, starting with data truth, then a replay UI.
**A:** Ingested Stimpee 3/4/6 to SQLite; standardised Z as negative TVDSS mSS so point-grid and trajectory align without a sign flip; preferred Petrel XYZ point-set export over CPS3 rasters after the raster missed the well path; built a FastAPI + React replay for Stimpee 6 (McKinlay top to 2 m below; 45/90 stations in the target window).
**R:** Phase 0 and Phase 1b are complete on a public repo. This is an independent tool, not a Santos production system. Use it to show method, not operator impact.
**Use for:** "Tell me about a time you integrated messy well data", "How do you support a drill-well programme?", "Give an example of initiative"

### 2. Cooper-Eromanga thermal history (basin / reservoir context)
**S:** The Cooper-Eromanga system has hydrocarbon and geothermal interest, but the Cretaceous thermal maximum was poorly constrained.
**T:** Contribute apatite fission-track, U-Pb, and geochemical work that feeds thermal-history models (Nixon, Fernie et al., 2024, *Basin Research*).
**A:** Applied the same AFT / LA-ICP-MS methods from the MPhil; interpreted detrital populations and heating/cooling paths with co-authors.
**R:** Peer-reviewed paper arguing radiogenic heating plus burial/thermal blanketing, not only a simple burial story. Directly relevant when a team asks "do you understand this basin, or only the well in front of you?"
**Use for:** "Describe your basin knowledge", "How does academic work transfer to an operator?"

### 3. First-author shear-zone reactivation (Scientific Reports, 2018)
**S:** The Bole-Nangodi shear zone in northern Ghana is interpreted as a continental extension of an equatorial Atlantic transform.
**T:** Constrain its low-temperature thermal history as Honours then as a first-author paper.
**A:** AFT data along the NE-SW trend; two-phase cooling (CAMP-related heating, then Cretaceous rift-shoulder exhumation); differential exposure north vs south of the zone.
**R:** *Scientific Reports* paper (Fernie et al., 2018). Shows independent scientific delivery and structural thinking.
**Use for:** "Tell me about a piece of work you owned end to end", "How do you handle structural problems?"

### 4. Wellsite year then geomechanics year (operations to mechanics)
**S:** Santos graduate path: wellsite geologist in Adelaide (2019), then geomechanist in Brisbane (2020-2021), then development geologist.
**T:** Learn operations geology first, then subsurface mechanics, then development.
**A:** (Fill with confidential well examples before interview.) Public fact is the sequence of titles, which is itself a coherent operations-to-development arc.
**R:** Seven-plus years in one operator, not a series of disconnected contracts.
**Use for:** "Walk me through your career", "Why development geology rather than research?"

<!-- Add more STAR examples as needed. Aim for 4-6 covering different competencies. -->

## Common Tough Questions

### "Why did you leave [previous company]?"
> Still at Santos. Frame a move as going toward global development-asset geoscience (KLTC supports ExxonMobil producing assets worldwide), not as an escape. Do not criticise Santos.

### "You don't have [specific skill/experience]."
> For quantitative seismic: "I have not been a QI specialist. I do interpret well logs, tops, trajectories, and Petrel-exported surfaces, and I would treat seismic as the next dataset in the same integration habit." For full static models: "I export and interrogate Petrel surfaces and well data. I have not owned a property-model build. That is a gap I would close in an integrated team, not something I will pretend is already done."

### "Where do you see yourself in 5 years?"
> Integrated development geoscientist who can sit with reservoir engineers on depletion planning and with drillers on well placement, with seismic and static-model literacy added on the job.

### "What's your biggest weakness?"
> Public CV is thin on confidential Santos metrics. In the room, give one real well example. On skills: seismic QI is the honest gap, already named.

### "Why this company specifically?"
> Customize per company. For ExxonMobil KL: KLTC as a global upstream support hub (corporate energy technology centers page; Malaysia operations page: two PETRONAS PSCs, ~40 platforms). The geoscientist posting is development and producing assets, which matches the Santos arc. Never give a generic "large IOC" answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission - this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
