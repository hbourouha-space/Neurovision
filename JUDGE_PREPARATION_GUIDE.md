# NeuroVision — Judge Preparation Guide

**Spaceflight Vision Research Platform**

A practical guide for judge Q&A, a live browser demo, and failed-demo recovery. Present NeuroVision as an early-stage research prototype. Its contribution is the way it connects observation workflows and simplified engineering concepts; it is not a medical device, anatomical simulation, NASA-connected platform, or regeneration technology.

## 30-second opening

NeuroVision is an early-stage research and engineering platform exploring how spaceflight-associated ocular changes, fluid dynamics, and tissue mechanics can inform questions about optic nerve health. The prototype has four workspaces: Daily Check-in, Periodic Measurements, Relationship Explorer, and a simplified CFD/FEA Workbench. It brings observation organization and engineering concepts into one research environment while making assumptions and limitations visible. NASA ocular datasets are identified as future research sources, not claimed as already integrated.

## What is actually implemented

| Workspace | Current capability | Important boundary |
|---|---|---|
| Daily Check-in | Records selected visual-symptom observations in the current session and displays a cautionary message. | Cannot diagnose, determine cause, provide medical clearance, or contact a medical team. |
| Periodic Measurements | Allows manual entries with assessment, domain, measurement, value, unit, eye/side, protocol, and notes. | Entries are session-only; no connected medical device or persistent patient record. |
| Relationship Explorer | Shows seven synthetic time points at 15-day intervals; displays raw measures separately and relative baseline-normalized indices. | Examples are synthetic. Normalization does not make different units equivalent. Correlation is not causation. |
| CFD / FEA Workbench | Calculates idealized rigid-tube laminar-flow quantities and a one-dimensional linear-elastic response proxy. | These are simplified mathematical teaching surrogates, not anatomical CSF CFD, an FEA mesh, or a validated optic-nerve model. |

## Likely judge questions and suggested answers

### 1. What problem are you addressing?
Spaceflight-associated ocular changes raise questions about visual function, ocular structure, fluid redistribution, and the mechanical environment around the optic nerve. Research observations can be fragmented across measurement types and studies. NeuroVision explores a common workflow for organizing observations and investigating possible physical mechanisms without pretending that the prototype establishes a cause.

### 2. What does NeuroVision do today?
It has four workspaces. Daily Check-in structures symptom observations; Periodic Measurements records manual entries with units and context; Relationship Explorer demonstrates how separate measures can be compared relative to their own baselines; and CFD/FEA Workbench runs two simplified engineering calculations. Built-in trend data are synthetic, and manual records are not connected to NASA or clinical systems.

### 3. Why combine vision measurements with CFD and FEA?
The observation workflow describes what may change over time. CFD and FEA offer engineering frameworks for asking how fluid conditions and mechanical loading could influence a modeled environment. The current calculations are simplified proxies. A future workflow would require appropriate anatomy, measured material properties, boundary conditions, verification, validation, and expert review before connecting model outputs to biological interpretation.

### 4. Is the CFD model simulating CSF around the optic nerve?
No. The current calculation is steady, laminar, Newtonian flow in a rigid circular tube using the Hagen–Poiseuille relationship. It is a transparent teaching proxy. It omits annular perioptic anatomy, pulsatility, compliant boundaries, tissue exchange, and validated physiological boundary conditions. It should not be described as anatomical CSF CFD.

### 5. What does the FEA workbench calculate?
It uses a one-dimensional homogeneous linear-elastic approximation: nominal strain equals stress divided by Young's modulus, and the displacement proxy is strain multiplied by a characteristic length. It is not a finite-element mesh, a tissue-specific optic-nerve model, or a coupled fluid-structure simulation.

### 6. Where do the relationship plots get their data?
The built-in demonstration contains seven synthetic points at 15-day intervals for four illustrative variables: venous-flow proxy, CSF-dynamics proxy, peripapillary thickness, and visual-function score. Each series is shown in its own raw units and also divided by its own initial value to create an index where baseline equals 100. These are examples—not astronaut data, patient records, or NASA datasets.

### 7. Why normalize every series to 100?
It makes relative change easier to visualize when variables have different units and scales. A value of 105 means five percent above that series' own starting value. It does not make micrometers, arbitrary scores, and flow proxies physically equivalent. Raw values are also kept separate.

### 8. Can correlations or time-lag analysis show what causes vision changes?
No. They demonstrate descriptive relationships in synthetic series. Correlation and lag alignment do not establish causation, physiological delay, or prediction. Real analysis would need valid measurements, appropriate sample sizes, protocol consistency, confounder handling, uncertainty estimates, and independent validation.

### 9. Have you integrated NASA OSDR datasets?
Not yet. NASA's Open Science Data Repository and Life Sciences Data Archive are candidate research sources. The project plan references ocular/translaminar study records for future review, but the current prototype does not automatically download or integrate those datasets. I distinguish candidate sources from data actually used.

### 10. Why is this relevant to optic nerve regeneration?
The long-term research motivation is to better understand the environment around the optic nerve—ocular structure, fluid conditions, and tissue mechanics—and formulate questions that could connect with biological research on retinal ganglion cells and axonal injury or repair. The current prototype does not regenerate nerves, prove a regeneration mechanism, or demonstrate vision restoration. Spaceflight ocular datasets alone are not regeneration datasets.

### 11. Is this an astronaut health-monitoring or diagnostic tool?
No. It is a research prototype. The check-in and measurement workspaces illustrate how observations can be structured. There is no medical-device connection, clinical validation, flight validation, patient-data storage, or diagnostic algorithm. It must not be used for medical or mission decisions.

### 12. What happens to manual entries?
In the current implementation, manual records are kept in the active application session. They are not sent to NASA, a clinical system, or a persistent patient database. The browser-based demonstration clears session records when the page is refreshed or closed.

### 13. What role did Super Intelligence or AI play?
ChatGPT supported ideation, research organization, writing, and coding/debugging during development. AI-generated concept visuals are part of the project's presentation assets and should be identified as such. The envisioned SI research agent is a future concept; there is no connected SI agent in the current prototype, and no NASA experimental data were generated or fabricated by AI.

### 14. What are the biggest limitations?
NASA data integration is not implemented; example data are synthetic; manual entries are session-only; CFD and FEA are simplified proxies; and the platform has not been clinically, anatomically, or flight validated. The goal today is to demonstrate a responsible research workflow and identify what would be needed for credible future models.

### 15. What would you build next?
First, review specific NASA study metadata and files and implement a traceable data layer that preserves study ID, species or model, instrument, protocol, units, and provenance. Next, develop anatomical and experimentally grounded CFD/FEA models with verification and validation. Then connect those results with appropriately selected biological evidence on retinal ganglion-cell survival and axonal injury or repair, with domain-expert review.

### 16. What is the personal motivation?
Share only what feels comfortable: “The project has a personal motivation connected to vision loss in my family. It made me want to contribute to research that could expand what scientists understand about vision and the optic nerve. I am careful to distinguish that long-term hope from what this prototype can currently demonstrate.”

### 17. What did you learn as a builder?
“I entered the challenge worried about coding, working from a Chromebook, and learning unfamiliar tools. I decided to learn by building rather than waiting until I felt fully ready. NeuroVision and PHOENIX are the two projects I brought to submission. The experience taught me to break a large idea into smaller workflows, make limitations explicit, and keep moving when the technology is unfamiliar.”

## Two-minute demo route

1. **Overview:** State the research aim and the four workspaces.
2. **Daily Check-in:** Select a symptom option and submit. Explain that the feedback is informational, not a diagnosis.
3. **Periodic Measurements:** Enter an example measurement with value, unit, eye/side, and protocol. Explain that it is session-only.
4. **Relationship Explorer:** Show the four synthetic series, toggle one off, and point out baseline = 100.
5. **CFD / FEA Workbench:** Change one tube-flow input and calculate; then calculate the one-dimensional elastic proxy. Explain assumptions and omissions.
6. **Close:** “The next step is traceable NASA data integration and validated, anatomically informed modeling—not a claim of clinical or regeneration capability today.”

## If the live demo fails

**Say:** “The original notebook dashboard was too heavy to load reliably in my Chromebook environment. I found an oversized embedded illustration inside the notebook source and removed that payload. I also prepared a lightweight browser dashboard so the four workspaces can be demonstrated without opening Colab or launching a Gradio server.”

Primary fallback — lightweight browser dashboard:
https://hbourouha-space.github.io/Neurovision/NeuroVision_Lightweight_Dashboard.html

Secondary fallback — seven-slide project demo:
https://hbourouha-space.github.io/Neurovision/NeuroVision_NASA_7_Slide_Demo.html

Repository:
https://github.com/hbourouha-space/Neurovision

Recovery:
1. Open the lightweight browser dashboard first. It uses plain HTML, CSS, and JavaScript and has no Gradio server or third-party runtime dependency.
2. Navigate through Overview, Daily Check-in, Periodic Measurements, Relationship Explorer, and CFD/FEA Workbench.
3. If the browser dashboard is unavailable, open the seven-slide presentation and explain the workflows using the diagrams and limitations.
4. If a judge wants implementation detail, show NeuroVision_COMMAND_CENTER.ipynb or NeuroVision_FINAL_BACKUP.ipynb in the repository.
5. Do not wait for a temporary Gradio share link during judging; it is not permanent hosting.

**What changed in the repository:** The large command-center notebook contained one embedded image as a code line of about 3.17 million characters. That payload was removed and replaced by a small CSS/HTML conceptual visual. The notebook was reduced from about 3.2 MB to about 28 KB while retaining the four workspaces and existing calculations. The new browser dashboard is an additional fallback, not a claim of clinical validation.

## Short answers for difficult moments

- **“Is this real astronaut data?”** No. Built-in relationship series are synthetic demonstration records.
- **“Does NASA data drive the plots?”** No. NASA OSDR and LSDA are candidate future sources, not integrated datasets.
- **“Is this true anatomical CFD?”** No. It is a rigid circular-tube laminar-flow calculation.
- **“Is this a real finite-element simulation?”** No. It is a one-dimensional linear-elastic proxy, not a mesh-based FEA solver.
- **“Can this restore vision?”** No. It is a research concept; regeneration and vision restoration are long-term motivations, not current capabilities.
- **“Will measurements persist?”** No. Manual entries are session-only in this version.
- **“What is the strongest current contribution?”** A coherent four-workspace research prototype with transparent engineering assumptions and clearly labeled boundaries.

## Phrases to avoid

Do not say NeuroVision detects or diagnoses SANS, monitors astronaut health in real time, connects to NASA systems, uses actual astronaut datasets in the plots, models the anatomical optic nerve, predicts clinical outcomes, regenerates nerves, or restores vision. Do not describe the planned SI agent as already implemented.

## Reference links

- Repository: https://github.com/hbourouha-space/Neurovision
- Lightweight browser dashboard: https://hbourouha-space.github.io/Neurovision/NeuroVision_Lightweight_Dashboard.html
- Seven-slide demo: https://hbourouha-space.github.io/Neurovision/NeuroVision_NASA_7_Slide_Demo.html
- NASA OSDR: https://osdr.nasa.gov/
- NASA Life Sciences Data Archive: https://lsda.jsc.nasa.gov/

**Final reminder:** NeuroVision does not need to be presented as a finished medical technology. Present it as a disciplined early-stage research prototype, show the four workspaces, explain the engineering proxies, and be transparent about synthetic data and future NASA integration.
