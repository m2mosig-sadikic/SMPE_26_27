# SMPE Homework — Paper Reviews

**Course:** SMPE  
**Task:** Read 11 papers (≤10–15 min each) and answer 3 questions per paper.

---

## Questions to answer for each paper

1. **Is this paper worth being read?**
2. **Is it a famous paper?**
3. **Any other point you would like to make?**

---

## Table of Contents

1. [The Anatomy of a Large-Scale Hypertextual Web Search Engine](#paper-1)
2. [Attention Is All You Need](#paper-2)
3. [On the Refinement of DHTs](#paper-3)
4. [Deep Latent Mixture Model for Recommendation](#paper-4)
5. [Paper 5 — *Title TBD*](#paper-5)
6. [Paper 6 — *Title TBD*](#paper-6)
7. [Paper 7 — *Title TBD*](#paper-7)
8. [Paper 8 — *Title TBD*](#paper-8)
9. [Paper 9 — *Title TBD*](#paper-9)
10. [Paper 10 — *Title TBD*](#paper-10)
11. [Paper 11 — *Title TBD*](#paper-11)

---

## Paper 1

**Title:** The Anatomy of a Large-Scale Hypertextual Web Search Engine  
**Authors:** Sergey Brin, Lawrence Page  
**Year:** 1998  

### Summary

This paper describes the design and implementation of Google, a large-scale web search engine built at Stanford. The key idea is to exploit the hyperlink structure of the web rather than relying only on keyword matching. Two main contributions: **PageRank**, an algorithm that ranks pages based on the number and quality of links pointing to them (inspired by academic citation analysis), and **anchor text propagation**, which uses the text of a hyperlink to describe the page it points to. The system also includes a distributed web crawler, an efficient inverted index, and a ranking function that combines multiple signals. The prototype indexed 24 million pages.

### Is this paper worth being read?

Yes. It is the founding paper of Google and introduces PageRank, which remains one of the most influential ideas in information retrieval. Even if the technical details are now outdated, the core concepts are essential to understanding how web search works.

### Is it a famous paper?

Extremely. It is one of the most cited papers in computer science, with tens of thousands of citations. Brin and Page published it while PhD students at Stanford, and it directly led to the creation of Google Inc. in 1998.

### Other remarks

The paper is honest about its limitations: the ranking function has many tunable parameters that the authors admit they haven't fully optimized. There is also a note in the appendix (not included in this printed version) warning about the conflict of interest between advertising revenue and search quality — surprisingly prescient given what the web advertising market became.

---

## Paper 2

**Title:** Attention Is All You Need  
**Authors:** Vaswani, Shazeer, Parmar, Uszkoreit, Jones, Gomez, Kaiser, Polosukhin (Google Brain / Google Research)  
**Year:** 2017 (NeurIPS)  

### Summary

This paper introduces the **Transformer**, a neural network architecture for sequence-to-sequence tasks (e.g. machine translation) that completely removes recurrence and convolutions, relying solely on attention mechanisms. The core idea is **self-attention**: each token in a sequence can directly attend to every other token, regardless of distance, in a constant number of operations. The architecture uses **multi-head attention** (several attention functions in parallel) and **positional encodings** (sine/cosine signals added to embeddings) to preserve word order. On English-German and English-French translation benchmarks (WMT 2014), the Transformer outperformed all previous models while training in a fraction of the time.

### Is this paper worth being read?

Absolutely. The Transformer is the foundation of virtually every modern large language model (BERT, GPT, T5, LLaMA, etc.). Understanding it is unavoidable for anyone working in NLP or deep learning.

### Is it a famous paper?

One of the most famous papers in the history of deep learning. It has over 100,000 citations and is widely considered one of the most impactful publications of the 2010s. The title itself has become iconic.

### Other remarks

The paper is remarkably well-written and self-contained. One interesting detail: the authors use sinusoidal positional encodings rather than learned ones, arguing it may generalize better to unseen sequence lengths — but experiments show the two perform nearly identically. The architecture was designed for translation but its success in NLP quickly inspired applications in vision (ViT), audio, and biology (AlphaFold).

---

## Paper 3

**Title:** On the Refinement of DHTs  
**Authors:** G. Michael, S.R. Sri Vidhya, D. Jayapriya (Bharath Institute of Higher Education, Tamilnadu)  
**Year:** 2019 (IJEAT)  

### Summary

The paper claims to present a system called "Despot" that refines Distributed Hash Tables (DHTs) using reinforcement learning and consistent hashing. It describes a framework with four components, runs some experiments, and draws conclusions about the incompatibility of superpages and semaphores. The writing is vague throughout, the experimental results are unexplained, and the references are almost entirely unrelated papers from the same journal issue — many co-authored by the same group.

### Is this paper worth being read?

No. This paper is a known example of **SCIgen-generated content** — SCIgen is a program that automatically generates fake computer science papers with random but plausible-sounding text. The abstract and body are nonsensical on close reading: sentences don't connect, claims are unjustified, and the "results" are meaningless. It was included here presumably as an exercise in critical reading.

### Is it a famous paper?

Not in a positive sense. It is not a credible research contribution. IJEAT (International Journal of Engineering and Advanced Technology) is a low-quality journal with no meaningful peer review. The paper has no legitimate academic impact.

### Other remarks

This paper is a great illustration of why critical reading matters. Red flags: buzzword-heavy abstract with no clear thesis, self-referential citation network (all 30 references are from the same journal), incoherent experimental setup, and conclusions that don't follow from any results. The prof likely included it deliberately to train exactly this kind of detection.

---

## Paper 4

**Title:** Deep Latent Mixture Model for Recommendation  
**Authors:** Jun Zhang, Ping Li, Wei Wang (Renmin University of China)  
**Year:** 2022 (arXiv preprint, under review)  

### Summary

The paper claims to propose a "cone latent mixture model" for recommendation systems. The introduction surveys related work on collaborative filtering and graph neural networks. The "Method" section then completely abandons the topic and presents abstract mathematical theorems about subalgebras, topoi, Pólya–Darboux conditions, and Noetherian domains — none of which has any connection to recommendation systems. The paper ends abruptly after two pages of pure abstract algebra with no experiments, no evaluation, and no conclusion.

### Is this paper worth being read?

No. This is another example of **automatically generated fake content**, this time combining two independent generators: a realistic-looking recommendation systems introduction (probably copy-pasted or lightly edited from real papers), and a mathematics paper generator similar to Mathgen. The two halves have nothing to do with each other. There is no actual method, no results, and no contribution.

### Is it a famous paper?

No. It is an arXiv preprint with no peer review, no citations, and no academic standing.

### Other remarks

This paper is a subtler trap than Paper 3: the introduction reads plausibly and cites real papers, which could fool a hasty reader. The break happens at Section 2 where the content becomes pure mathematical nonsense unrelated to the title. It illustrates that checking only the abstract and introduction is not enough — the method section needs to be read too.

---