"# RGB_Benchmarking-implentation-of-LLM-s" 
An implementation for [Benchmarking Large Language Models in Retrieval-Augmented Generation](https://arxiv.org/abs/2309.01431)
Retrieval-Augmented Generation Benchmark

The data is placed in the data/ directory:

data/
├── en.json
├── en_refine.json
├── en_int.json
├── en_fact.json

To evaluate Information Integration, use en_int.json.

To evaluate Counterfactual Robustness, use en_fact.json.

The Refined Data

The refined dataset includes:

Removal of incorrect positive and negative documents.

Addition of relevant positive documents.

Correction of inaccurate answers.

Evaluation

The evaluation process involves assessing model accuracy, rejection rates, and error detection. The outputs include:

all_rate: Accuracy (when noise_rate < 1) or rejection rate (noise_rate = 1).

fact_check_rate: Error detection rate (ED).

reject_rate: Rejection rate (Rej*).

correct_rate: Error correction rate (CR).
