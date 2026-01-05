# PersonalityDBench: Sample Data for Reviewers

This repository contains a **sample subset** of the PersonalityDBench dataset, provided exclusively for **peer review purposes** to allow reviewers to examine the data structure, annotation format, and quality without requiring a full data use agreement .

## ⚠️ Important Notice

**This is NOT the full dataset.** The complete PersonalityDBench resource will be released upon paper acceptance, subject to a data use agreement that ensures ethical use and user privacy protection

## 📋 Overview

**PersonalityDBench** is the first large-scale, clinician-annotated dataset for modeling and generating personality disorders (PDs) from digital footprints. It comprises two complementary components:

1. **PRISMA** (PeRsonality dISorder MAnifestations): A clinically annotated collection of Reddit content spanning the full spectrum of PDs, integrating SCID-5-PD diagnostic criteria and HiTOP trait dimensions.

2. **PersonaDSteering**: A standardized benchmark for evaluating LLM steering toward clinically grounded PD profiles via structured behavioral elicitation tasks.


Personality disorders represent complex mental health conditions characterized by persistent patterns of cognition, behavior, and emotional regulation. Despite their prevalence (4.4–21.5% in Western populations) and clinical significance, computational research has largely overlooked PDs in favor of more common conditions like depression or anxiety.

**PersonalityDBench** addresses this gap by providing:
- **Clinical annotations** of 155 Reddit users across 10 PD categories (Cluster A, B, C)
- **SCID-5-PD criterion-level** evidence classification 
- **HiTOP trait-level** annotations mapping posts to dimensional psychopathology constructs
- **15,268 reference answers** (11 conditions: 10 PDs + baseline) for benchmarking

---
## 🗂️ Sample Dataset Structure

```rsonalityDBench/
├──PRISMA_sample
|    ├── user_sample
|    
├──PersonaDSteering
   |    ├── QAs_sample |    ├── test_questions |         ├──test_questions_sample_NPD |         ├──test_questions_sample_PPD
└── README.md-```-

## 🗂️ Original Dataset Structure

```rsonalityDBench/
├── PRISMA/
│   ├── users_metadata.json          # User-level demographics and diagnoses
│   ├── scid_annotations/            # SCID-5-PD criterion evidence (per user)
│   ├── hitop_annotations/           # HiTOP trait labels (per post)
│   └── posts/                       # Anonymized Reddit posts and comments
│
├── PersonaDSteering/
│   ├── questions/                   # 1,388 structured test questions
│   ├── reference_answers/           # 15,268 aligned PD-conditioned + baseline answers
│   └── steering_vectors/            # Pre-computed CAA steering vectors (optional)
│
└── README.md
```

