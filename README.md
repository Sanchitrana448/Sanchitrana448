<h1 align="center">Sanchit Rana</h1>

<p align="center">
  <b>AI / ML engineer in training. I build systems that say when they might be wrong, and publish the evidence.</b><br>
  MSc Artificial Intelligence, University of Bath (dissertation: Distinction, 71)
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/sanchit--rana">LinkedIn</a> ·
  <a href="https://github.com/Sanchitrana448?tab=repositories">All repositories</a>
</p>

---

## Open to

Graduate AI, machine learning and MLOps roles, and remote AI/ML internships (UK and India).

## Three projects, each live, tested and reproducible

Every project has a live demo, CI on every push, and a one-command evaluation that regenerates its `RESULTS.md`. The numbers below come from those files, not from me.

### 1. ResearchPilot AI: a research assistant that checks its own citations
[Repo](https://github.com/Sanchitrana448/researchpilot-ai) · [Live demo](https://researchpilot-ai-yw7y.onrender.com) · ![tests](https://github.com/Sanchitrana448/researchpilot-ai/actions/workflows/ci.yml/badge.svg)

- **Problem:** many RAG demos cite sources that do not exist or do not support the claim.
- **What I built:** a 7-stage pipeline (planner, retrieval, ranking, contradiction check, synthesis, citation validator, quality control) that verifies every citation against the evidence actually retrieved, and refuses to answer when there is none.
- **Result:** 8/8 retrieval hits and 0 invalid citations on a fixed eval; about 5 ms server-side.
- **Honest limit:** TF-IDF retrieval, so it matches words, not meaning. Dense embeddings are the next step.

### 2. DocMind AI: document extraction that knows when it got it wrong
[Repo](https://github.com/Sanchitrana448/docmind-ai) · [Live demo](https://docmind-ai-8uct.onrender.com) · ![tests](https://github.com/Sanchitrana448/docmind-ai/actions/workflows/ci.yml/badge.svg)

- **Problem:** OCR errors such as `$24.50` read as `$2450` look like valid data, so they pass silently.
- **What I built:** OCR, classification and field extraction with a confidence score per field, validation rules, and a human review step.
- **Result:** across 32 generated documents, including blurred and downscaled scans, 0 wrong totals or dates were returned without being sent to review.
- **Honest limit:** extractors are rules, so unusual layouts will fail. A layout-aware model is the next step.

### 3. MLForge: a churn pipeline with the parts that usually get skipped
[Repo](https://github.com/Sanchitrana448/mlforge) · [Live demo](https://mlforge-o15e.onrender.com) · ![tests](https://github.com/Sanchitrana448/mlforge/actions/workflows/ci.yml/badge.svg)

- **Problem:** a model with a good ROC-AUC (0.76 on the test set) can still be useless. At the default threshold it caught only 30% of churners.
- **What I built:** data validation, a three-way split, a versioned model registry, a FastAPI service, drift detection and a cost-based threshold analysis.
- **Result:** choosing the threshold on validation data raised test recall from 0.30 to 0.90 and cut total cost by 48%, under stated cost assumptions.
- **Honest limit:** the data is synthetic and the cost model assumes every retention offer works.

> The demos run on a free tier, so the first request after a quiet period can take up to a minute to wake.

## How I work

- **Measure, then claim.** Every number above comes from a file you can regenerate.
- **Write down the limits.** Every README has a Limitations section.
- **Fail loudly.** Where a result is uncertain, the system flags it instead of guessing.

## Tools

`Python` · `FastAPI` · `scikit-learn` · `Tesseract OCR` · `Docker` · `GitHub Actions` · `pytest`
