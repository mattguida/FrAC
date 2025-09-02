# FrAC: From Articles to Comments
## A Framework for Computational Framing Analysis across Text Types

[![Paper](https://img.shields.io/badge/paper-TACL-blue)](link-to-paper)
[![Model](https://img.shields.io/badge/🤗%20Hugging%20Face-Model-yellow)](link-to-model)
[![License](https://img.shields.io/badge/License-CC%20BY%204.0-green.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository contains the data and models for "From Articles to Comments: A Framework for Computational Framing Analysis" (XXX).

## Overview
We present the first computational framework for large-scale analysis of framing patterns across source content (e.g., news articles) and audience responses (e.g., reader comments). 
We implement sentence-based frame classification and topic identification methods.
Our approach examines how readers engage with, retain, or reframe media content across 11 topics and 2 news outlets -- [The New York Times](https://www.kaggle.com/datasets/aashita/nyt-comments) (NYT) and the [SFU Opinion Corpus](https://github.com/sfu-discourse-lab/SOCC) (SOCC)

## Datasets
### 1. FrAC (Frames in Articles and Comments) Corpus
- **File**: gold_standard_single_label_all.csv
- **Content**: more than 500 manually annotated sentences from articles and comments
- **Annotation**: 9 frame categories - and an "Other" category - with high inter-annotator agreement (α=0.76)
  
### 2. Large-Scale Framing Effects Dataset
- **Files**: nyt_all.csv, socc_all.csv
- **Content**: 2,776 articles and 386,090 comments across 11 topics
- **Topics**: Gun Control, Russia-Ukraine, Trump & Elections, Healthcare, Immigration, LGBT+ Rights, Education, Abortion, Israel-Palestine, Climate Change, Syria & IS
- **Info**: Articles and comments in this data are aligned by same topic to allow for analysis of framing patterns when the comments stay on topic. Each article and comment is also annotated with a dominant frame label, automatically assigned with out fine-tuned sentence frame classifier.

## 📊 Key Statistics

| Dataset | Articles | Comments | Topics | Timeframe |
|---------|----------|----------|---------|-----------|
| NYT     | 1,699    | 346,476  | 11      | 2017-2018 |
| SOCC    | 1,077    | 39,614   | 11      | 2012-2016 |

**Licensing Note**: The sentences are drawn from the SOCC Corpus (CC BY 4.0), and the NYT Corpus (CC BY-NC-SA 4.0)
We release our annotations under the same license. Please cite both our work and the original corpora. 


## Model Released

Frame Classifier

### Frame Classifier
- **Model**: Fine-tuned RoBERTa-Large 
- **Training**: 63K sentences across articles and comments
- **Performance**: F1=0.77 (articles), F1=0.83 (comments)
- **HuggingFace**: [XXX](link-to-model)

```python
from transformers import pipeline

classifier = pipeline("text-classification", model="your-org/frac-frame-classifier")
result = classifier("The new immigration policy will boost economic growth.")
```

## 🏷️ Frame Categories

Our framework uses 9 frame categories derived from the Media Frames Corpus:

1. **Legality and Crime** - Legal aspects, law enforcement
2. **Political and Policies** - Political processes, policy solutions  
3. **Economic** - Financial costs, economic impacts
4. **Health and Safety** - Public health, safety concerns
5. **Cultural Identity** - Social groups, cultural values
6. **Public Opinion** - Popular sentiment, polls
7. **Morality** - Ethics, moral imperatives
8. **Fairness and Equality** - Justice, equal treatment
9. **Security and Defense** - National security, military
10. **Other**
  

# Citation
XXX

