# Linguistic Metadata Model (LMM)
Version 1.0 • Draft

The Linguistic Metadata Model defines the linguistic, historical, and structural metadata standards used across the Bulgarian Language & Script Corpus (BLSC). It ensures consistent tagging, historical alignment, and long-term compatibility with NLP pipelines and academic use.

---

## 1. Purpose

The LMM provides a unified schema for:
- historical period classification,
- orthographic variants,
- linguistic layers (morphology, syntax, normalization),
- dialectal and regional markers,
- metadata needed for ML datasets,
- compatibility with UD, TEI, ISOcat.

---

## 2. Historical Periodization of Bulgarian (1800–present)

### 2.1. Early Modern Bulgarian (1800–1878)
Characteristics:
- transitional orthography,
- Church Slavonic influence,
- inconsistent spelling.

Metadata fields:
- orthography: early_modern
- dialect_influence: yes/no
- source_type: manuscript/print

---

### 2.2. Transitional Period after Liberation (1878–1899)
Metadata fields:
- orthography: transitional_1878
- jat_usage: full/reduced/absent
- etymological_spelling: partial

---

### 2.3. Pre-Reform Official Standard (1899–1945)
Metadata fields:
- orthography: pre_reform_1899
- obsolete_letters: ["ѣ","ѫ","ѧ","ъi"]
- normalization_needed: yes/no

---

### 2.4. Post-Reform Orthography (1945–1990)
Metadata fields:
- orthography: post_reform_1945
- spelling_modernization: minimal

---

### 2.5. Contemporary Bulgarian (1990–present)
Metadata fields:
- orthography: modern
- internet_register: yes/no
- loanword_stage: naturalized/raw

---

## 3. Dialect Classification (Optional)

Values:
- western
- eastern
- rupian
- shopluk
- pirin_macedonian
- other

Field:
- dialect: value_or_null

---

## 4. Linguistic Layers

| Layer | Field | Description |
| morphology | morph_layer | POS + morph tags |
| syntax | syntax_layer | dependency relations |
| lemma | lemma_layer | lemma alignment |
| ner | ner_layer | named entities |
| phonetic | phonetic_layer | historic/optional |
| normalization | normalized_text | machine-normalized version |

---

## 5. Metadata Schema Example (JSON)

```json
{
  "id": "blsc_00001231",
  "author": "Иван Вазов",
  "year": 1894,
  "period": "pre_reform_1899",
  "orthography": "pre_reform_1899",
  "dialect": null,
  "genre": "fiction",
  "source_type": "print",
  "script": "Cyrillic",
  "token_count": 1520,
  "morph_layer": false,
  "syntax_layer": false,
  "normalized_text": null,
  "rights": "public_domain"
}

6. Genre Classification

fiction

journalism

academic

legal

administrative

scientific

religious

personal documents

folklore

internet

other



---

7. Normalization Versions

v1: historical → modern baseline

v2: historical → machine-normalized

v3: OCR-normalized + spellcheck


Field: normalization_version


---

8. Future Extensions (2025–2026)

extended morphological tagsets,

lemma dictionary harmonization,

dialect embeddings,

OCR ground truth dataset,

tokenizer training corpora.



---

9. Revision Policy

Updates require:

1. Issue discussion


2. Maintainer approval


3. Version bump


4. Backward compatibility review




---

End of Document
