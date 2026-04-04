<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=180&section=header&text=Ashmit%20Singh&fontSize=42&fontColor=fff&animation=twinkling&fontAlignY=32&desc=I%20build%20systems%20that%20think%20%E2%80%94%20and%20interfaces%20worth%20using&descAlignY=55&descSize=15"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=20&duration=3000&pause=800&color=A855F7&center=true&vCenter=true&width=700&lines=ML+%26+Computer+Vision+Engineer;Flutter+%2B+Systems+Developer;Architecture-first.+Accuracy-obsessed.;From+loss+curves+to+button+radius.)](https://git.io/typing-svg)

<p>
  <a href="https://www.linkedin.com/in/ashmitsingh04112005/"><img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:connect.ashmit.singh@proton.me"><img src="https://img.shields.io/badge/-ProtonMail-6D4AFF?style=flat-square&logo=protonmail&logoColor=white"/></a>
  <a href="mailto:connect.ashmit.singh@outlook.com"><img src="https://img.shields.io/badge/-Outlook-0078D4?style=flat-square&logo=microsoft-outlook&logoColor=white"/></a>
  <img src="https://komarev.com/ghpvc/?username=Ashmit-Singh&color=A855F7&style=flat-square&label=Profile+Views"/>
</p>

</div>

---

## `> identity`

```python
class Ashmit(MLEngineer, MobileDeveloper, SystemsDesigner):
    """
    I sit at the intersection of ML research and product engineering.
    I don't just train models — I design the systems around them.
    """

    education    = "B.Tech CS @ SRM IST (2024–2028)  |  CGPA: 8.90 / 10"
    focus        = ["Computer Vision", "On-device ML", "Production Flutter"]
    internships  = ["Mobile App Dev @ Singsys Pvt. Ltd. (Production Codebase)"]

    engineering_style = {
        "design_first":     "I prototype interfaces before writing a single line of logic",
        "depth_over_demos": "I care about why the loss stalls, not just that it converged",
        "real_constraints": "My projects handle messy data, tight latency, small datasets",
    }

    currently = "Applying to IIT research programs · Deepening PyTorch internals"
    open_to   = "ML/CV research internships · Hard problems with messy data"
```

Second-year CS student who has shipped production Flutter screens at Singsys, built CV pipelines on real clinical data, and architected a distributed drug-safety system — not a toy. I think in systems: caching strategies, failure modes, deployment constraints. The UX is never an afterthought.

---

## Projects

> Each project below was chosen because it required a non-trivial engineering decision — not just assembling libraries.

---

### 🛡️ Drug Safety Guard &nbsp;·&nbsp; [GitHub](https://github.com/Ashmit-Singh/drug-safety-guard)

**The problem:** Most drug-interaction checkers compare brand names. That is insufficient — the same active ingredient appears under dozens of formulations. A doctor signing off on a polypharmacy prescription needs ingredient-level safety, in real time.

**The hard part:** Naive pairwise checking across all ingredient combinations is O(n²·m²) — catastrophically slow for a UX that must feel instant. I solved this by pre-computing ingredient interaction pairs and caching them in Redis with a 24-hour TTL, reducing lookup time to sub-millisecond even on complex prescriptions.

**The architecture:** PostgreSQL + Supabase RLS enforced across 14 tables for access control. Cassandra audit trail with 2-year retention — correctness here is a compliance requirement, not a feature. Docker + Kubernetes for reproducible deployment. The data model separates drug entities, formulations, and ingredient linkages so the detection logic is swappable without touching storage.

`Flutter` `Node.js` `PostgreSQL` `Redis` `Cassandra` `Supabase` `Docker` `Kubernetes`

---

### 🔬 Psoriasis Severity Classifier &nbsp;·&nbsp; [GitHub](https://github.com/Ashmit-Singh)

**The problem:** 13-class severity classification on ~886 images. A regime where architecture choices, augmentation strategy, and ensemble design matter far more than compute.

**The hard part:** With a dataset this small, overfitting is the default outcome. I trained an EfficientNetB0 + DenseNet121 ensemble, using each model's different inductive biases as a natural regulariser. Augmentation was calibrated to simulate real-world clinical photo variance — angle, lighting, skin tone. Achieved **88% validation accuracy** at this scale.

**Why it matters:** This is the anchor project across my research applications. It demonstrates that I understand the constraints that make small-data CV hard, not just how to run a training loop.

`PyTorch` `EfficientNetB0` `DenseNet121` `OpenCV` `Scikit-learn`

---

### 📄 Document Vision Pipeline &nbsp;·&nbsp; [GitHub](https://github.com/Ashmit-Singh)

**The problem:** Real-world documents are not clean scans. They arrive skewed, shadowed, low-contrast, in variable fonts — and OCR pipelines break on all of it.

**The solution:** A staged pipeline where each component handles one failure mode. YOLOv8 localises document regions to handle partial captures. OpenCV corrects skew and contrast before OCR sees a single pixel. Tesseract extracts text from a normalised input. Each stage is independently tunable — degradation in one does not cascade downstream.

`YOLOv8` `OpenCV` `Tesseract OCR` `Python`

---

### 🔍 Semantic Search Engine &nbsp;·&nbsp; [GitHub](https://github.com/Ashmit-Singh)

Dense retrieval over custom corpora using FAISS + Sentence Transformers — no vector database dependency, no external API calls. Embeddings are indexed locally for approximate nearest-neighbour search at millisecond latency. The design choice was deliberate: self-contained, auditable, and deployable without cloud infrastructure.

`FAISS` `Sentence Transformers` `Python`

---

### 📷 Cross-Platform QR Scanner &nbsp;·&nbsp; [Live Demo](https://qr-scanner-nu-six.vercel.app)

Single Flutter codebase targeting Android, iOS, Linux, macOS, and Web — deployed on Vercel. No permissions bloat, no tracking, no unnecessary dependencies. Built as a proof that Flutter's cross-platform promise holds when you don't cut corners on it.

`Flutter` `Dart` `Vercel`

---

## Experience

**Singsys Private Limited — Mobile App Developer Intern** &nbsp;·&nbsp; 2025 &nbsp;·&nbsp; Lucknow

Worked inside a production Flutter codebase — not a side project. Shipped multiple responsive UI screens, integrated RESTful APIs with async state management, and resolved cross-device UI and logic bugs ahead of a hard production deadline. Learned what "production-ready" actually means when real users are on the other end.

---

## Stack

| Domain | Technologies |
|---|---|
| **Languages** | Python · C++ · Java · Dart · SQL · LaTeX |
| **ML / CV** | PyTorch · Scikit-learn · OpenCV · YOLOv8 · Tesseract OCR · FAISS · Sentence Transformers · NumPy · Pandas |
| **Mobile** | Flutter · Dart |
| **Backend & Infra** | Node.js · PostgreSQL · Redis · Cassandra · Docker · Kubernetes · Supabase |
| **Tools** | Git · Linux · Jupyter · VS Code · Figma · Kaggle |

---

## Currently

Extending the psoriasis classifier toward a cleaner research artifact — better ablation documentation, reproducible training scripts, and a sharper writeup on why ensemble design outperforms single-model scaling at this data scale. Applying to IIT summer research programs. Going deeper into PyTorch internals: not just calling `.fit()`, but understanding how architectural choices interact with small, imbalanced datasets at the gradient level.

**Open to:** ML/CV research internships where the problems are hard, the data is messy, and engineering judgment matters as much as benchmark scores.

---

## Engineering Philosophy

```
Design is the first layer of engineering, not the last coat of paint.

Readable code beats clever code — a codebase is a communication medium
between engineers across time, not a performance for the compiler.

If the interface needs a tutorial, the design already failed.

Optimise for the human first. The machine will keep up.
```

---

## GitHub Analytics

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Ashmit-Singh&show_icons=true&hide_border=true&bg_color=0D1117&title_color=A855F7&icon_color=A855F7&text_color=ffffff&rank_icon=github" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ashmit-Singh&layout=compact&hide_border=true&bg_color=0D1117&title_color=A855F7&text_color=ffffff&langs_count=8" height="165"/>

</div>

<div align="center">
<img src="https://streak-stats.demolab.com?user=Ashmit-Singh&theme=transparent&hide_border=true&border_radius=8&background=0D1117&ring=A855F7&fire=A855F7&currStreakLabel=A855F7&sideLabels=ffffff&dates=888888" height="150"/>
</div>

---

<div align="center">

**Open to ML / CV research internships and hard engineering problems.**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ashmitsingh04112005/)
[![ProtonMail](https://img.shields.io/badge/ProtonMail-6D4AFF?style=for-the-badge&logo=protonmail&logoColor=white)](mailto:connect.ashmit.singh@proton.me)
[![Outlook](https://img.shields.io/badge/Outlook-0078D4?style=for-the-badge&logo=microsoft-outlook&logoColor=white)](mailto:connect.ashmit.singh@outlook.com)

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer"/>

</div>
