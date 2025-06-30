# Computational Framework for Analyzing Framing Patterns across Text Types

## 📊 Datasets Released

### 1. FrAC (Frames in Articles and Comments) Corpus
- **Size**: 530 manually annotated sentences
- **Content**: 265 article sentences + 265 comment sentences  
- **Annotations**: 10-category frame taxonomy with inter-annotator agreement
- **Purpose**: Gold-standard benchmark for cross-genre frame classification
- **Format**: JSON with sentence text, frame labels, and metadata

### 2. SOCC-NYT Framing Effects Dataset  
- **Size**: 2,776 articles + 386,090 comments across 11 topics
- **Sources**: The Globe and Mail (SOCC) + New York Times (NYT)
- **Content**: Pre-processed articles and comments with:
  - Dominant frame predictions
  - Topic assignments (11 categories)
  - On-topic article-comment alignments
  - Framing effect labels (retention/reframing patterns)
- **Purpose**: Large-scale framing effects analysis
- **Topics**: Gun Control, Russia-Ukraine, Trump & Elections, Healthcare, Immigration, LGBT+ Rights, Education, Abortion, Israel-Palestine, Climate Change, Syria & IS

The sentences in this dataset are drawn from the [SOCC Corpus](https://github.com/sfu-discourse-lab/SOCC), licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).
We release our annotations and the corresponding texts under the same license. If you use our annotated corpus, you must cite both our work and the original SOCC corpus.

## 🤖 Models Released

- **Fine-tuned RoBERTa-Large Frame Classifier**: Trained on 63K sentences, achieves F1=0.81 on cross-genre evaluation. The model is available on HuggingFace: XXX


# Citation
XXX
