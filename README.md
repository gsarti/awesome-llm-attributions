# A Survey of Attributions for Large Language Models

## 🌟 Introduction

Open-domain dialogue systems, driven by large language models, have changed the way we use conversational AI. 
However, these systems often produce content that might not be reliable. In this repo, we focus on summarizing where these systems get their facts from, a process known as attribution or citation. We look at where the facts come from, how they are used by the models, how well these methods work, and datasets and challenges like unclear knowledge sources, biases, and over-attribution.

## 1. Attribution Definition & Position Paper
*   [2021/07] **Rethinking Search: Making Domain Experts out of Dilettantes** *Donald Metzler et al. arXiv.* [[paper](https://arxiv.org/pdf/2105.02274.pdf)] 

     <!-- ```
      This position paper says "For example, for question answering tasks our envisioned model is able to synthesize a singleanswer that incorporates information from many documents in the corpus, and it will be able to support assertions in the answer by referencing supporting evidence in the corpus, much like a properly crafted Wikipedia entry supports each assertion of fact with a link to a primary source. This is just one of many novel tasks that this type of model has the potential to enable." 
      ```--> 
*   [2023/03] **TRAK: Attributing Model Behavior at Scale** *Sung Min Park et al. arXiv.* [[paper](https://arxiv.org/abs/2303.14186)][[code](https://github.com/MadryLab/trak)]
      <!--```
      Attributing Model: trace model predictions back to training data. This paper introduces a data attribution method that is both effective and computationally tractable for large-scale, differentiable models.
      ```-->

*   [2023/07] **Citation: A Key to Building Responsible and Accountable Large Language Models** *Jie Huang et al. arXiv.* [[paper](https://arxiv.org/pdf/2307.02185.pdf)] 
      <!--```
      This position paper embarks on an exploratory journey into the potential of integrating a citation mechanism within large language models, examining its prospective benefits, the inherent technical obstacles, and foreseeable pitfalls.
      ```-->

*   [2023/09] **ChatGPT Hallucinates when Attributing Answers** *Guido Zuccon et al. arXiv.* [[paper](https://arxiv.org/abs/2309.09401)]
      <!--```
      This paper suggests that ChatGPT provides correct or partially correct answers in about half of the cases (50.6% of the times), but its suggested references only exist 14% of the times. In thoses referenced answers, the reference often does not support the claims ChatGPT attributes to it.
      ```-->



## 2. Attribution Paper Before the Era of Large Language Models 

### 2.1 Fact Checking & Claim Verificication
*   [2021/08] **A Survey on Automated Fact-Checking**  *Zhijiang Guo et al. TACL'22*  [[paper](https://arxiv.org/pdf/2108.11896.pdf)]

*   [2021/10] **Truthful AI: Developing and governing AI that does not lie** *Owain Evans et al. arXiv* [[paper](http://arxiv.org/abs/2110.06674)]

*   [2021/05] **Evaluating Attribution in Dialogue Systems: The BEGIN Benchmark** *Nouha Dziri et al. TACL'22* [[paper](https://aclanthology.org/2022.tacl-1.62/)][[code](https://github.com/google/BEGIN-dataset)]

### 2.2 Feature Attribution and Interpretability of Models for NLP 
*   [2022/12] **Foveate, Attribute, and Rationalize: Towards Physically Safe and Trustworthy AI** *Alex Mei et al. findings of ACL'22* [[paper](https://aclanthology.org/2023.findings-acl.701.pdf)]

## 3. Sources of Attribution

### 3.1 Pre-training Data
* [2023/02] **The ROOTS Search Tool: Data Transparency for LLMs** *Aleksandra Piktus et al. arXiv.* [[paper](https://arxiv.org/pdf/2302.14035.pdf)]
* [2022/05] **ORCA: Interpreting Prompted Language Models via Locating Supporting Data Evidence in the Ocean of Pretraining Data** *Xiaochuang Han et al. arXiv.* [[paper](https://arxiv.org/pdf/2205.12600.pdf)]

* [2022/05] **Understanding In-Context Learning via Supportive Pretraining Data** *Xiaochuang Han et al. arXiv.* [[paper](https://arxiv.org/pdf/2306.15091.pdf)]
### 3.2 Out-of-model Knowledge


## 4. Datasets for Attribution
* [2022/12] **CiteBench: A benchmark for Scientific Citation Text Generation** *Martin Funkquist et al. arXiv.* [[paper](https://arxiv.org/abs/2212.09577)]


* [2023/05] **Enabling Large Language Models to Generate Text with Citations** *Tianyu Gao et al. arXiv.* [[paper](https://arxiv.org/pdf/2305.14627.pdf)] [[code](https://github.com/princeton-nlp/ALCE)]
   <!--```
   This paper proposes ALCE dataset, which collects a diverse set of questions and retrieval corpora and requires building end-to-end systems to retrieve supporting evidence and generate answers with citations.
   ```-->

* [2023/07] **HAGRID: A Human-LLM Collaborative Dataset for Generative Information-Seeking with Attribution** *Ehsan Kamalloo et al. arXiv.* [[paper](https://arxiv.org/pdf/2307.16883.pdf)] [[code](https://github.com/project-miracl/hagrid)]
   <!--```
   This paper introduces the HAGRID dataset for building end-to-end generative information-seeking models that are capable of retrieving candidate quotes and generating attributed explanations.
   ```-->
* [2023/09] **EXPERTQA : Expert-Curated Questions and Attributed Answers** *Chaitanya Malaviya et al. arXiv.* [[paper](https://arxiv.org/pdf/2309.07852.pdf)] [[code](https://github.com/chaitanyamalaviya/expertqa)]
   <!--```
   This paper introduces the EXPERTQA, a high-quality long-form QA dataset with 2177 questions spanning 32 fields, along with verified answers and attributions for claims in the answers. 
   ```-->


## 5. Approaches to Attribution

### 5.1 Direct Generated Attribution

### 5.2 Retrieval-then-Answering

### 5.3 Post-Generation Attribution

*  [2022/10] **RARR: Researching and Revising What Language Models Say, Using Language Models** *Luyu Gao et al. arXiv.* [[paper](https://arxiv.org/abs/2210.08726)]

*  [2023/04] **The Internal State of an LLM Knows When its Lying** *Amos Azaria et al. arXiv.* [[paper](http://arxiv.org/abs/2304.13734)]
      <!--```
      This paper utilizes the LLM's hidden layer activations to determine the veracity of statements by a classifier receiveing as input the activation values from the LLM for each of the statements in the dataset.
      ```-->
*  [2023/05] **Do Language Models Know When They're Hallucinating References?** *Ayush Agrawal et al. arXiv.* [[paper](http://arxiv.org/abs/2305.18248)]

*  [2023/05] **Complex Claim Verification with Evidence Retrieved in the Wild** *Jifan Chen et al. arXiv.*  [[paper](https://arxiv.org/abs/2305.11859)][[code](https://github.com/jifan-chen/fact-checking-via-raw-evidence)]
      <!--```
      This paper proposes a pipeline(claim decomposition, multi-granularity evidence retrieval, claim-focused summarization) to improve veracity judgments.
      ```-->
*  [2023/06] **Retrieving Supporting Evidence for LLMs Generated Answers** *Siqing Huo et al. arXiv.*  [[paper](http://arxiv.org/abs/2306.13781)]
      <!--```
      This paper proposes a two-step verification. The LLM's answer and the retrieved document queried by question and LLM's answer are compared by LLM, checking whether the LLM's answer is hallucinated.
      ```-->



### 5.4 Attribution Systems & End-to-End Attribution Models

* [2022/03] **LaMDA: Language Models for Dialog Applications** *Romal Thoppilan et al. arXiv.* [[paper](https://arxiv.org/pdf/2201.08239.pdf)]

*  [2022/03] **WebGPT: Browser-assisted question-answering with human feedback** *Reiichiro Nakano, Jacob Hilton, Suchir Balaji et al. arXiv.*[[paper](https://arxiv.org/pdf/2112.09332.pdf)]

*  [2022/03] **GopherCite - Teaching language models to support answers with verified quotes**  *Jacob Menick  et al. arXiv.* [[paper](http://arxiv.org/abs/2203.11147)]

## 6. Attribution Evaluation
*   [2021/12] **Measuring Attribution in Natural Language Generation Models.** *H Rashkin et al. CL.* [[paper](https://arxiv.org/pdf/2112.12870.pdf)]
      <!--```
      This paper presents a new evaluation framework entitled Attributable to Identified Sources (AIS) for assessing the output of natural language generation models.
      ```-->
*   [2022/12] **Attributed Question Answering: Evaluation and Modeling for Attributed Large Language Models.** *B Bohnet et al. arXiv.* [[paper](https://arxiv.org/pdf/2212.08037.pdf)] [[code](https://github.com/google-research-datasets/Attributed-QA)]
*   [2023/04] **Evaluating Verifiability in Generative Search Engines** *Nelson F. Liu et al. arXiv.* [[paper](http://arxiv.org/abs/2304.09848)]

*   [2023/05] **Evaluating and Modeling Attribution for Cross-Lingual Question Answering** *Benjamin Muller et al. arXiv.* [[paper](https://arxiv.org/abs/2305.14332)]
*   [2023/05] **FActScore: Fine-grained Atomic Evaluation of Factual Precision in Long Form Text Generation** *Sewon Min et al. arXiv.* [[paper](https://arxiv.org/abs/2305.14251)] [[code](https://github.com/shmsw25/FActScore)]

*   [2023/05] **"According to ..." Prompting Language Models Improves Quoting from Pre-Training Data** *Orion Weller et al. arXiv.*  [[paper](https://arxiv.org/abs/2305.13252)]
      <!--```
      This paper proposes according-to prompting to directing LLMs to ground responses against previously observed text, and propose QUIP-Score to measure the extent to which model-produced answers are directly found in underlying text corpora.
      ```-->
*   [2023/05] **Automatic Evaluation of Attribution by Large Language Models.** *X Yue et al. arXiv.* [[paper](https://arxiv.org/pdf/2305.06311.pdf)] [[code](https://github.com/OSU-NLP-Group/AttrScore)]
      <!--```
      This paper investigate the automatic evaluation of attribution by LLMs - AttributionScore, by providing a definition of attribution and then explore two approaches for automatic evaluation. The results highlight both promising signals as well as remaining challenges for the automatic evaluation of attribution.
      ```-->
*   [2023/07] **FacTool: Factuality Detection in Generative AI -- A Tool Augmented Framework for Multi-Task and Multi-Domain Scenarios** *I-Chun Chern et al. arXiv.* [[paper](https://arxiv.org/abs/2307.13528v2)][[code](https://github.com/GAIR-NLP/factool)]


## 7. Limitations, Future Directions and Challenges in Attribution

      a. hallucination of fact attribution
      b. Inability to attribute  parameter knowledge of model self
      c. Validity of the knowledge source, some evidence may be wrong
      d. Bias in attribution method
      e. Over-attribution & under-attribution

***For finding survey of hallucination please refer to:***

- Siren's Song in the AI Ocean: A Survey on Hallucination in Large Language Models
- Cognitive Mirage: A Review of Hallucinations in Large Language Models
- A Survey of Hallucination in Large Foundation Models


## Project Maintainers & Contributors
- Dongfang Li 
- Zetian Sun
- Xinshuo Hu
- Zhenyu Liu
