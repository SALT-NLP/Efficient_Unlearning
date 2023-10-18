
# 📜 Efficient_Unlearning

🔍 This is the official code and data repository for the EMNLP 2023 paper titled "Unlearn What You Want to Forget: Efficient Unlearning for LLMs".

* The codes will be updated soon.

## 🌟 Abstract

<details><summary>Abstract</summary>

Large language models (LLMs) have achieved significant progress from pre-training on and memorizing a wide range of textual data, however, this process might suffer from privacy issues and violations of data protection regulations. As a result, the ability to easily remove data related to individual users from such models while not deteriorating their predictive quality after the removal becomes increasingly important. To address these issues, in this work, we propose an efficient unlearning framework that could efficiently update LLMs without having to retrain the whole model after data removals, by introducing lightweight unlearning layers learned with a selective teacher-student objective into the transformers. In addition, we introduce a fusion mechanism to effectively combine different unlearning layers that learns to forget different sets of data to handle a sequence of forgetting operations. Experiments on classification and generation tasks demonstrate the effectiveness of our proposed methods compared to the state-of-the-art baselines.

</details>


## 📊 Data Description

📥 **Download Data**: [Download Link]

## 🚀 How to Run

### Environment Setup
```
conda install mpi4py
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
pip install -e improved-diffusion/ 
pip install -e transformers/
pip install spacy==3.2.4
pip install datasets==1.8.0 
pip install huggingface_hub==0.4.0 
pip install wandb
```

### 🧠 Single Unlearn

```
python src/run.py --unlearn --forgot_data "forgot.csv" --retained_data "retained.csv"
```

### 🌐 Fusing Unlearning Layers

```
python src/run.py --merge --merge_set "the folder of the weights to merge"
```
