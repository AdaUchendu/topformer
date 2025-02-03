# TopFormer: Topology-Aware Authorship Attribution of Deepfake Texts with Diverse Writing Styles #
Recent advances in Large Language Models (LLMs) have enabled the generation of open-ended high-quality texts, that are non-trivial to distinguish from human-written texts. We refer to such LLM-generated texts as deepfake texts. There are currently over 72K text generation models in the huggingface model repo. As such, users with malicious intent can easily use these open-sourced LLMs to generate harmful texts and dis/misinformation at scale. To mitigate this problem, a computational method to determine if a given text is a deepfake text or not is desired–i.e., Turing Test (TT). In particular, in this work, we investigate the more general version of the problem, known as Authorship Attribution (AA), in a multi-class setting–i.e., not only determining if a given text is a deepfake text or not but also being able to pinpoint which LLM is the author. We propose TopFormer to improve existing AA solutions by capturing more linguistic patterns in deepfake texts by including a Topological Data Analysis (TDA) layer in the Transformer-based model. We show the benefits of having a TDA layer when dealing with imbalanced, and multi-style datasets, by extracting TDA features from the reshaped pooled_output of our backbone as input. This Transformer-based model captures contextual representations (i.e., semantic and syntactic linguistic features), while TDA captures the shape and structure of data (i.e., linguistic structures). Finally, TopFormer, outperforms all baselines in all 3 datasets, achieving up to 7% increase in Macro F1 score. 




# Dependencies #
The code base requires Python 3.9 and Packages are in *requirements.txt*.
For the TDA features, we use: https://github.com/aidos-lab/pytorch-topological

# Problem Definition #
<img src="AA.jpg" alt="drawing" style="width:750px;"/>
Illustration of the Authorship Attribution (AA) problem with multiple authors - human and many LLM authors

# Models #
* BERT
* TopBERT_pool
* TopBERT_attn
* Gaussian-BERT
* RoBERTa
* Gaussian-RoBERTa
* TopFormer
* TopFormer_attn

# Datasets #
You can download these datasets here:
- SynSciPass: https://github.com/domenicrosati/synscipass/tree/main/data


# Cite us #
```
@incollection{uchendu2024topformer,
  title={Topformer: Topology-aware authorship attribution of deepfake texts with diverse writing styles},
  author={Uchendu, Adaku and Le, Thai and Lee, Dongwon},
  booktitle={ECAI 2024},
  pages={1446--1454},
  year={2024},
  publisher={IOS Press}
}

