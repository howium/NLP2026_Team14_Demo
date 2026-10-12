# NLP2026 Team 14 — Track B (Demonstration)

**From Bag-of-Words to Large Language Models: A Unified Comparative System for Text Classification**

Course project for Natural Language Processing (Nankai University, Fall 2026).
Team 14 · Jiahao Wu (Student ID: 2113454) · solo team.

## Project Overview

**ClassiScope** integrates four text-classification model families under a single data protocol, evaluation suite, and web interface:

1. **Sparse lexical features** — bag-of-words / TF-IDF + logistic regression
2. **Static word embeddings** — Word2Vec / GloVe mean-pooled document vectors + logistic regression
3. **Pretrained transformers** — fine-tuned BERT-base
4. **Instruction-tuned LLMs** — zero-/few-shot prompting (Qwen2.5 via API, small local variant as fallback)

The project asks *when model sophistication actually pays off*: the four routes are compared on identical data splits (Accuracy, Macro-F1), stress-tested for robustness, probed with token-level explanations, and profiled for efficiency (parameters, training time, latency). Evaluation: news topic classification on the course-provided NYT news subset, plus sentiment classification on SST-2.

## Repository Structure

```
├── proposal/            # Phase 1: Project Proposal
│   ├── Team14_Proposal.pdf
│   └── latex/           # LaTeX sources (ACL official template)
├── requirements.docx    # Original course project requirements (Chinese)
└── README.md
```

## Building the Proposal PDF

Requires any TeX distribution with pdfLaTeX and BibTeX (tested on TeX Live 2022, WSL Ubuntu 22.04):

```bash
cd proposal/latex
pdflatex main && bibtex main && pdflatex main && pdflatex main
```

## Status

- [x] **Phase 1** — Project Proposal (due 2026-10-12)
- [ ] **Phase 2** — Midterm milestone (date TBD): four model routes, preliminary results, demo skeleton
- [ ] **Phase 3** — Final report (8-page ACL format), final slides, demo/video, source code (dates TBD)

Source code, experimental results, and the final report will be added in later phases.
