# NeuroVision Wear

## Spaceflight Vision Research Platform

**From microgravity ocular research to optic nerve protection and
regeneration research**

NeuroVision is an early-stage research and engineering prototype
designed to bring together longitudinal vision-related measurements,
spaceflight ocular research, and computational engineering concepts. Its
long-term ambition is to help researchers investigate the physical and
biological environment surrounding the optic nerve and formulate better
questions about optic nerve protection, injury, and future regeneration
research.

> **Scientific boundary:** NeuroVision does not diagnose disease,
> predict clinical outcomes, demonstrate optic nerve regeneration, or
> provide validated astronaut-health monitoring. The current application
> includes synthetic demonstration records and simplified engineering
> calculations. NASA data integration and anatomically validated
> multiphysics modeling are future development goals.

![NeuroVision scientific
architecture](assets/neurovision_primary_architecture.png)

## Why NeuroVision?

Spaceflight-associated fluid redistribution and other physiological
changes motivate research into ocular structure, visual function,
cerebrospinal-fluid (CSF) dynamics, and the optic nerve environment.
NeuroVision is built around two connected research needs:

1.  **Observe and organize change over time.** Bring daily observations
    and periodic ocular measurements into a common longitudinal view
    while preserving each measurement's units, source, eye/side, device,
    and protocol.
2.  **Investigate possible physical mechanisms.** Use computational
    fluid dynamics (CFD) and finite element analysis (FEA) concepts to
    explore fluid behavior and tissue mechanics that may be relevant to
    optic nerve health.

The longer-term research ambition is to connect spaceflight ocular
evidence and engineering models with biological research relevant to
retinal ganglion-cell survival, axonal injury, neuroprotection, and
optic nerve regeneration. Microgravity ocular datasets can inform the
study of the environment and mechanisms; they do **not**, by themselves,
demonstrate nerve regeneration.

## Personal motivation and long-term purpose

NeuroVision is also rooted in a deeply personal motivation. The project was inspired in part by the user's experience as a parent of a child affected by retinoblastoma, a childhood eye cancer that resulted in the loss of her daughter's eye. That experience strengthened the user's commitment to the broader goal of vision restoration.

The ultimate long-term aspiration behind NeuroVision is to contribute to research that may one day support vision restoration through optic nerve regeneration. This is an ambitious research goal, not a capability of the current application and not a claim that optic nerve regeneration can currently be achieved through this platform. Retinoblastoma treatment, eye loss, optic nerve injury, and retinal ganglion-cell/axon regeneration are distinct clinical and biological contexts; the project should not imply that optic nerve regeneration alone reverses the consequences of eye removal.

The personal motivation should be presented respectfully and only as much as the user wishes to disclose in a public submission.

## What the current prototype demonstrates

The current Colab/Gradio prototype presents four main areas:

-   **Daily Check-in:** a structured place for daily observations.
-   **Periodic Measurements:** manual logging of research or
    clinician-supervised measurements with units, eye/side, device, and
    protocol context.
-   **Relationship Explorer:** aligns measurements on a common mission
    timeline and compares relative change using each series' own
    baseline. The example graph normalizes each series to 100 at
    baseline; it does not make unlike units physically equivalent.
-   **CFD/FEA Workbench:** an early engineering research workbench
    containing simplified mathematical proxies, including a simplified
    flow calculation and a one-dimensional elastic-deformation
    calculation.

The current workbench is **not** a full anatomical optic-nerve CFD
model, a validated tissue FEA model, or a coupled fluid-structure
interaction simulation. It should be presented as an
educational/research concept and a starting point for future model
development.

![Monitoring and engineering
concept](assets/neurovision_monitoring_engine.png)

## How CFD and FEA add research value

### CFD --- Computational Fluid Dynamics

CFD provides a framework for investigating fluid behavior in a modeled
perioptic environment. Depending on the geometry, boundary conditions,
and validated inputs available in a future model, outputs could include:

-   Fluid velocity and flow patterns
-   Pressure distribution and pressure gradients
-   Wall shear stress

**Research question:** How might changes in the fluid and pressure
environment around the optic nerve alter local mechanical conditions?

### FEA --- Finite Element Analysis

FEA provides a framework for investigating how modeled tissues respond
to mechanical loading. With appropriate anatomical geometry and
experimentally supported material properties, outputs could include:

-   Tissue displacement
-   Stress distribution
-   Strain fields
-   Sensitivity to material stiffness and loading assumptions

**Research question:** Under what modeled loading conditions might
ocular or perioptic tissues experience different levels of deformation
or stress?

### The future coupled workflow

A future multiphysics workflow could use CFD-derived pressure or fluid
loads as inputs to an FEA model. The resulting modeled mechanical
conditions could then be compared with longitudinal ocular observations
and relevant biological evidence. Such comparisons would generate
hypotheses and guide further experiments; they would not establish
causation or diagnose an individual.

![CFD, FEA and regeneration research
visual](assets/neurovision_regeneration_pathway.png)

## From microgravity ocular data to optic nerve regeneration research

NeuroVision's long-term ambition is not limited to monitoring
astronauts. It is to use spaceflight and related experimental research
as one source of evidence for understanding the optic nerve environment.

A responsible research pathway could include:

1.  **Characterize ocular changes:** organize longitudinal OCT/RNFL,
    visual-function, imaging, and other measurements where available.
2.  **Study the surrounding environment:** examine relevant CSF,
    pressure, and fluid-dynamics evidence from spaceflight and
    ground-based models.
3.  **Investigate tissue mechanics:** use anatomically informed FEA
    models to explore stress and deformation under clearly stated
    assumptions.
4.  **Integrate biological evidence:** examine relevant retinal
    ganglion-cell, axonal, gene-expression, histology, and protein
    findings from suitable studies.
5.  **Generate testable hypotheses:** identify mechanisms and
    experimental questions relevant to optic nerve protection, neuronal
    survival, axonal repair, and future regeneration research.

**Important:** Spaceflight ocular datasets are not direct regeneration
datasets. Findings from animal studies, ex vivo human tissue,
computational models, and astronaut observations must remain
distinguishable. They have different experimental contexts and cannot be
treated as interchangeable evidence.

## Proposed research-data sources

The following NASA resources are relevant candidates for future
integration. Availability, licensing, data dictionaries, file formats,
and individual study contents should be checked before importing data.

-   **NASA Open Science Data Repository (OSDR):** https://osdr.nasa.gov/
-   **NASA Life Sciences Portal:** https://lsda.jsc.nasa.gov/
-   **OSD-815, OSD-816, OSD-817 and OSD-818:** related ocular /
    translaminar research records discussed in the project research
    plan. Verify each study's current metadata and downloadable files
    directly in OSDR before use.
-   **NASA spaceflight ocular research:** use individual study records
    and their associated publications to preserve species, experimental
    model, mission, assay, and measurement context.

The project should never imply that all these datasets are already
connected to the current application.

## Future Superintelligence (SI) research agent

A future development goal is to connect NeuroVision to a **Superintelligence (SI) research agent**. This agent is envisioned as a research assistant operating over curated, traceable sources—not as an autonomous medical decision-maker.

Potential future functions include:

- Find and summarize relevant NASA ocular and spaceflight studies.
- Help organize study metadata, measurement definitions, units, species, experimental models, and provenance.
- Compare longitudinal measurements and clearly distinguish observed data from synthetic examples and model outputs.
- Explain CFD/FEA scenario assumptions and summarize sensitivity analyses.
- Connect computational findings with relevant biological evidence on retinal ganglion cells, axons, neuronal survival, injury, and regeneration research.
- Generate research questions and hypotheses with source citations, uncertainty flags, and links to the underlying evidence.

The SI agent is **planned, not implemented** in the current prototype. Its outputs would require human scientific review, preserve source traceability, and must not diagnose, recommend treatment, claim clinical validity, or present speculative regeneration hypotheses as established findings.

## Current status and roadmap

  -----------------------------------------------------------------------
  Area                                Current status
  ----------------------------------- -----------------------------------
  Colab/Gradio application shell      Prototype exists

  Daily check-in and periodic         Present in prototype
  measurement workflow                

  Baseline-normalized relationship    Present; demonstration data are
  graph                               synthetic

  Simplified CFD calculation          Present as a mathematical proxy

  Simplified 1D elastic calculation   Present as a mathematical proxy

  NASA OSDR integration               Planned; not yet connected

  Anatomical optic-nerve CFD          Future work

  Anatomical ocular/optic-nerve FEA   Future work

  Coupled CFD--FEA model              Future work

  Biological regeneration evidence    Future work
  integration                         

  Clinical or flight validation       Not performed
  -----------------------------------------------------------------------

### Recommended next development steps

1.  Preserve the existing working notebook and document its exact
    version and dependencies.
2.  Add a curated, traceable NASA research-data layer with study IDs,
    source links, species/model, units, and provenance.
3.  Replace synthetic example records with clearly labeled imported
    research data only after checking their meaning and quality.
4.  Improve CFD/FEA inputs: geometry, boundary conditions, material
    properties, units, solver assumptions, and verification tests.
5.  Build a transparent comparison view that separates measured
    observations from model outputs.
6.  Develop a biological evidence module for retinal ganglion cells,
    axons, neuroprotection, and regeneration-related research.
7.  Seek domain-expert review before making physiological or clinical
    interpretations.

## How to run the prototype

The current prototype was developed in Google Colab and uses Python,
Gradio, Pandas, and Plotly. The exact notebook and dependency versions
should be included in this repository when the final app file is
exported from the owner's Google Drive.

1.  Open the notebook in Google Colab.
2.  Review and run the notebook cells in order.
3.  Launch the Gradio interface from the application cell.
4.  Use the temporary public Gradio URL only for a short demonstration.
    It is not permanent hosting.

**Repository packaging note:** Add the verified
`NeuroVision_FINAL_BACKUP.ipynb` file to the repository root before
publishing. The notebook is not embedded in this documentation package
because the live Google Drive notebook has not been exported into this
workspace.

## Responsible-use statement

NeuroVision is a research concept and prototype. It is not a medical
device, diagnostic tool, clinical decision-support system, or validated
predictor. Synthetic data must remain labeled as synthetic. Manual
entries are not connected to medical devices or NASA systems unless a
future integration is explicitly implemented and documented. All model
outputs must identify assumptions, units, uncertainty, and validation
status.

## Visual concept gallery

![Futuristic NeuroVision research
concept](assets/neurovision_futuristic_research.png)

![NeuroVision regeneration research
pathway](assets/neurovision_regeneration_pathway.png)

## Suggested citation and acknowledgement

NASA datasets and publications used in future versions should be cited
individually with their official study identifiers, dataset versions,
DOI or source URLs, and access dates. Do not cite the general NASA
portal as a substitute for the specific dataset used.

------------------------------------------------------------------------

**Project status:** Early-stage prototype and research concept\
**Focus:** Spaceflight ocular research, optic nerve environment,
computational engineering, and future neuroregeneration research

## The Builder's Journey

This challenge began with a practical uncertainty: I was worried about coding, working from a Chromebook, and learning unfamiliar tools. I chose to keep going, learn by building, and bring two engineering and research projects to submission for NASA Space Apps.

NeuroVision is one of those two projects. Together with PHOENIX, it represents a personal learning journey in which curiosity, persistence, and a willingness to tackle unfamiliar technology turned two ideas into submitted research and engineering prototypes. Both projects are early-stage work, with their capabilities and limitations documented openly. The journey is still continuing.
