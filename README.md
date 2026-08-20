# Neural Information Retrieval, Ranking, and RAG

Sanitised implementation notebooks from an information-retrieval project. The work compares classical lexical retrieval, neural reranking, dense retrieval, learned sparse retrieval, and retrieval-augmented generation.

## What is included

- Biomedical retrieval: a hand-built BM25 baseline, parameter tuning, and a BERT cross-encoder reranker evaluated on TREC-COVID.
- Web-passage retrieval: BM25, DPR, and TILDEv2 compared on a course-supplied MS MARCO sample, followed by a TinyLlama-based RAG experiment.
- Bonus experiments retained as a separate notebook.

## Recorded results

For the biomedical task, the recorded nDCG@10 was 0.5819 for the baseline BM25, 0.6338 for tuned BM25 (`k1=1.8`, `b=0.5`), and 0.6932 for the neural reranker. For the web-passage sample, recorded mean nDCG@3 was 0.599894 for BM25, 0.649346 for DPR, and 0.765001 for TILDEv2.

These are historical results from the supplied course datasets and experiment environment; they are not claims of performance on new data.

## Repository layout

- `notebooks/README.md` — a publication-safe summary of the notebook implementations and their recorded results.
- `data/` — data-access guidance only; no course data, queries, qrels, indexes, models, or outputs are included.

## Reproducing the work

Install the packages in `requirements.txt`, then obtain the required datasets and retrieval assets through their official sources and under the applicable licences. Runtime requirements may include Java for Pyserini and substantial compute/storage for neural models. The original notebooks are not published because they still contain course-specific configurations and assets that cannot be redistributed.

## Academic and data note

This public copy intentionally excludes assignment briefs, notebooks, answers, datasets, relevance judgements, indexes, trained assets, and generated outputs. It provides a transparent method summary and recorded aggregate results instead of redistributing course material.

## Author

Neha Elsa Renji — Master of Data Science student, The University of Queensland.
