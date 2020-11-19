# The overview of the awesome causality dataset 

The overview is about the decription of causality dataset, which is widely applied in causality relevant tasks, such as the semEval challenges.

## SemEval series
	SemEval (Semantic Evaluation) is an ongoing series of evaluations of computational semantic analysis systems; it evolved 
	from the Senseval word sense evaluation series. Started from SemEval-2007 to SemEval-2020. ---Wikipedia
	
### Dataset-1 (SemEval-2010 Task 8: Multi-Way Classification of Semantic Relations Between Pairs of Nominals.)

The dataset is used in the paper [[1]](#1), [[6]](#6), the relations from the dataset are classified into 10 categories:
- Cause-effect
- Component-whole
- Entity-destination
- Entity-origin
- Product-producer
- Member-collection
- Message-topic
- Content-container
- Instrument-agency
- Other

**Example**:

	Sentence: ”The current view is that the chronic <e1>inflammation</e1> in the distal part of the stomach caused by 
		   Helicobacter pylori <e2>infection</e2> results in an increased acid production from the non-infected 
		   upper corpus region of the stomach.”
	Cause-Effect: (e2,e1)
	Comment:
Dataset Github: https://github.com/sahitya0000/Relation-Classification

Dataset Paper: https://www.aclweb.org/anthology/S10-1006.pdf

**Comment**:
	The causal pairs can be used directly by selecting cause-effect relation only.
	
### Dataset-2 (SemEval-2012 Task #7: COPA: Choice Of Plausible Alternatives.)

Open-domain commonsense reasoning (COPA), focusing specifically on commonsense causal reasoning about everyday events. The Dataset is used in the paper[[3]](#3).

**Example**:

	Premise: The man broke his toe. What was the CAUSE of this? 
	Alternative 1: He got a hole in his sock. 
	Alternative 2: He dropped a hammer on his foot.

**Pre-processing**:

	Effect Event: <man, broke, toe>
	False Cause Event 1: <Hole, sock>
	True Cause Event 2: <Dropped, hammer, foot>
	
Dataset Website: https://www.cs.york.ac.uk/semeval-2012/task7/index.html

Dataset Paper: https://www.aclweb.org/anthology/S12-1052.pdf

### Dataset-3 (SemEval-2020 Task5: Modelling Causal Reasoning in Language: Detecting Counterfactuals.)

**Example**:

	sentence: If that was my daughter, I would have asked If I did something wrong.
	antecedent: If that was my daughter
	consequent: I would have asked If I did something wrong.
	antecedent_start: 0
	antecedent_end: 22
	consequent_start: 23
	consequent_end: 67

**Pre-preprocessing**:

	Conditional/Hypothetical Cause event: <was, my daughter>
	Effect event: <asked, did, wrong>

Dataset Website: https://competitions.codalab.org/competitions/21691


## Event denotation:

## Causal Pairs Extraction Methods:

### 1. Pattern (Causal cues) Extraction：
**Example**:

![Test Image 1](Causalcues.jpg)

## The above datasets are from following references：

<a id="1">[1]</a> Kyriakakis, Manolis, Ion Androutsopoulos, and Artur Saudabayev. "Transfer Learning for Causal Sentence Detection." arXiv preprint arXiv:1906.07544 (2019). [link](https://arxiv.org/abs/1906.07544)

<a id="2">[2]</a> Hashimoto, Chikara, et al. "Toward future scenario generation: Extracting event causality exploiting semantic relation, context, and association features." Proceedings of the 52nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers). 2014. [link](https://www.aclweb.org/anthology/P14-1093.pdf)

<a id="3">[3]</a> Kozareva, Zornitsa. "Cause-effect relation learning." Workshop Proceedings of TextGraphs-7: Graph-based Methods for Natural Language Processing. 2012. [link](https://www.aclweb.org/anthology/W12-4107.pdf)

<a id="4">[4]</a> Tanaka, Shohei, et al. "Conversational Response Re-ranking Based on Event Causality and Role Factored Tensor Event Embedding." arXiv preprint arXiv:1906.09795 (2019). [link](https://arxiv.org/pdf/1906.09795)

<a id="5">[5]</a> Xia, Rui, and Zixiang Ding. "Emotion-cause pair extraction: a new task to emotion analysis in texts." arXiv preprint arXiv:1906.01267 (2019).[link](https://arxiv.org/pdf/1906.01267)

<a id="6">[6]</a> Luo, Z., Sha, Y., Zhu, K. Q., Hwang, S. W., & Wang, Z. (2016, April). Commonsense Causal Reasoning between Short Texts. In KR (pp. 421-431).[link](http://www.cs.sjtu.edu.cn/~kzhu/papers/kzhu-copa.pdf)
