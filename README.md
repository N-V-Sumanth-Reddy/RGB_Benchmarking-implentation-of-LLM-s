# RGB Benchmarking - Implementation of LLMs

This repository contains an implementation for the paper [Benchmarking Large Language Models in Retrieval-Augmented Generation](https://arxiv.org/abs/2309.01431). The project focuses on evaluating the effectiveness of Large Language Models (LLMs) in Retrieval-Augmented Generation (RAG) using various benchmarking datasets.

## 📂 Data Structure
The dataset files are located in the `data` directory and are structured as follows:

```
data
├── en.json           # Main dataset
├── en_refine.json    # Refined dataset
├── en_int.json       # Information Integration dataset
├── en_fact.json      # Counterfactual Robustness dataset
```

### 📝 Dataset Descriptions
- **`en_int.json`**: Used to evaluate Information Integration.
- **`en_fact.json`**: Used to evaluate Counterfactual Robustness.
- **`en_refine.json`**: The refined dataset, which includes:
  - Removal of incorrect positive and negative documents.
  - Addition of relevant positive documents.
  - Correction of inaccurate answers.

## 📊 Evaluation Metrics
The evaluation process involves assessing model accuracy, rejection rates, and error detection. The following metrics are used:

- **`all_rate`**: Represents accuracy when `noise_rate < 1`, or rejection rate when `noise_rate = 1`.
- **`fact_check_rate`**: Error detection rate (ED).
- **`reject_rate`**: Rejection rate (Rej*).
- **`correct_rate`**: Error correction rate (CR).

## 🚀 Usage
### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-repo/RGB_Benchmarking.git
cd RGB_Benchmarking
```

### 2️⃣ RUN the ipynb file

Run all the cells in the ipynb file so that you can use gradio app to evaluate in the last cell.


### 3️⃣ Run the Evaluation

Initially please add your own API Keys of the LLM models in the config.ini file. Select the paramaters and model to evaluate the model will automatically fetch the data set required form the data config folder that is placed in the drive if the data config file dosen't exist in the drive please download and upload in the drive. Also select the input parameters in the gradio app.


## 📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

---

For more details, refer to the original research paper: [Benchmarking Large Language Models in Retrieval-Augmented Generation](https://arxiv.org/abs/2309.01431).
