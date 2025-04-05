# CREDIFY Framework
This project focuses on automating the fact-checking process for verifying open-domain claims. It utilizes expert-written justification articles to verify the veracity of these claims, aiming to improve the efficiency and accuracy of fact-checking procedures.

# RECTIFY Dataset
The complete dataset is located in RECTIFY Dataset folder in excel file 'Dataset_with_evidences.xlsx'. The dataset consists of open-domain claims with meta-data which can be verified against expert-written justification article. We also provide seperate evidence corpus in file evidence_corpus for further analysis.

## Environment:
We perform all the experiment on Google colab with python 3.11.11 installed. Install the transformer library with the following command.
```bash 
!pip install transformers 
!pip install sentence_transformers
```

# Experiments and Evaluation
The proposed framework CREDIFY consists of three modules : passage retrieval , sentence selection and veracity prediction. We applied two types of Data Augmentation Conrastive Claim generation and Paraphrazing. The following sections describe the detail of modules for implementing experiment.

1. Passage Retrieval and Varacity prediction: This folder consists of two jupyter notebooks, one is for passage retrievel where we used [`msmarco-distilbert-base-tas-b`](https://huggingface.co/sentence-transformers/msmarco-distilbert-base-tas-b) which is freely avialable on hugging face. For Veracity Prediction we used [`roberta-base`](https://huggingface.co/FacebookAI/roberta-base), we fine-tuned the model on our dataset and then used it for prediction.

2. Data Augmentation: This folder consists of two jupyter notebooks, where we applied two types of data augmentation techniques Contrastive claim generation and Parapharasing. For parapharasing we used chatgpt's [`T5_base`](https://huggingface.co/humarin/chatgpt_paraphraser_on_T5_base) model.

3. 5 fold cross validation: This folder consists of one jupyter notebook, where we applied 5 fold cross validation for better generalization. We also obtained time performance.

If you find this code helpful please cite our paper:

@article{nasir2025credify,
  title={CREDIFY: contextualized retrieval of evidence for open-domain fact verification},
  author={Nasir, Ayesha and Wasim, Muhammad and Nasir, Sarah},
  journal={Knowledge and Information Systems},
  pages={1--31},
  year={2025},
  publisher={Springer}
}

