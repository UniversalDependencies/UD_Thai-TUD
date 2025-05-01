# Summary

*UD Thai TUD* (Thai Universal Dependency Treebank) consists of 3,627 syntactic trees annotated using the Universal Dependencies framework. Documents were randomly sampled from the Thai National Corpus and Thai Wikipedia, covering various types such as news articles, Wikipedia articles, essays, advertisement, interviews, andstories. TUD covered diverse topics, such as politics, crime, entertainment, sport, history, religion, culture, and science.

# Introduction

The *UD Thai TUD* treebank was created to provide a broad-coverage syntactic resource for the Thai language under the Universal Dependencies (UD) framework. Text was randomly sampled from two major sources: the Thai National Corpus and the November 2020 dump of Thai Wikipedia. To ensure diversity, 5,000 paragraphs were selected from various document types—news articles, Wikipedia entries, essays, advertisements, interviews, and stories—covering a wide range of topics such as politics, crime, entertainment, sports, history, religion, culture, and science. After annotation and rigorous quality control, 3,627 well-formed dependency trees were retained in the final dataset.

## Annotation Process

All paragraphs were tokenized using the `newmm` tokenizer from the PyThaiNLP library, then annotated on the Datasaur platform. A team of 10 annotators with linguistics backgrounds was trained to: (1) correct tokenization errors, (2) assign Universal POS (UPOS) tags, (3) identify dependency arcs, and (4) label relations (DEPREL) without subtypes. The LEMMA field was excluded due to the lack of inflectional morphology in Thai.

Following pilot annotations and manual review, two annotators demonstrating the highest accuracy were selected to complete the remaining data. Agreement was evaluated on 20 double-annotated sentences (399 tokens), achieving Cohen’s Kappa scores of 0.92 (UPOS) and 0.84 (DEPREL), and UAS/LAS scores of 0.85 and 0.78. The annotated data was then converted into CoNLL-U format and split into individual trees based on dependency structure. Trees with incomplete labels, multiple roots, or structural errors were corrected, with additional quality assurance performed via manual inspection of 50 randomly selected trees.

## Train–Test Split

The final treebank was split into training, development, and test sets in an 8:1:1 ratio. It consists of syntactically complete trees rather than full documents. While Filenames are used to identify source paragraphs, typically reflecting their origin from the Thai National Corpus or Wikipedia. However, sentence IDs in the final treebank do not encode genre or domain metadata.
<center>

| UPOS  | Train | Dev  | Test | UPOS  | Train | Dev | Test |
|-------|-------|------|------|-------|-------|-----|------|
| NOUN  | 18777 | 2270 | 2310 | CCONJ | 2063  | 239 | 270  |
| VERB  | 14881 | 1802 | 1867 | ADJ   | 1575  | 223 | 197  |
| ADP   | 4517  | 530  | 560  | PART  | 1366  | 156 | 169  |
| ADV   | 4498  | 557  | 521  | NUM   | 1161  | 165 | 118  |
| AUX   | 3424  | 401  | 421  | DET   | 1140  | 137 | 144  |
| PRON  | 2796  | 322  | 350  | PUNCT | 871   | 104 | 125  |
| SCONJ | 2438  | 321  | 335  | SYM   | 16    | 1   | 1    |
| PROPN | 2488  | 293  | 295  |       |       |     |      |

*Table 1. UPOS Distribution in Each Split of TUD*



# Acknowledgments

TUD was developed as part of the paper *"The Thai Universal Dependency Treebank"*, published in *Transactions of the Association for Computational Linguistics (TACL)*. We thank the reviewers and the action editor of the paper for their constructive feedback, which contributed to significant improvements. We also gratefully acknowledge all annotators for their effort and dedication throughout the annotation process.

This work was supported by the National Research Foundation, Singapore under its AI Singapore Programme, and by the National Science Research and Innovation Fund (NSRF) through the Program Management Unit for Human Resources & Institutional Development, Research, and Innovation [grant number B0SF640234].

## References

If you use TUD in your project or publication, please cite as follows:

BibTex

```
@article{Sriwirote-etal-2024-TUD,
  title={The Thai Universal Dependency Treebank},
  author={Panyut Sriwirote and Wei Qi Leong and 
  Charin Polpanumas and Santhawat Thanyawong  and 
  William Chandra Tjhi and Wirote Aroonmanakun and 
  Attapol T. Rutherford},
  journal={Transactions of the Association for Computational Linguistics},
  year={in press},
  publisher={MIT Press Direct}
}
```


# Changelog

* 2025-05-15 v2.16
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.16
License: CC BY-SA 4.0
Includes text: yes
Genre: grammar-examples
Lemmas: not available
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Sriwirote, Panyut; Leong, Wei Qi; Polpanumas, Charin; Thanyawong, Santhawat; Tjhi, William Chandra; Aroonmanakun, Wirote; Rutherford, Attapol T.; Maitreenukul, Punyanuch
Contributing: here
Contact: attapol.t@chula.ac.th, punyanuch.maitree@gmail.com
===============================================================================
</pre>
