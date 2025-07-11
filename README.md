# Efficient X-Ray Representations For Classifying Diseases

## UBC Medicine Datathon 2025 (Team 8)

### Team Members:

#### My Main contributions to the team:
  - **Pinecone ETL**: ETL data pipeline to process **100+** Gb of Lung X-ray images for efficient "similar" vector retrieval
  - **EfficientNet-v5**: ResNet-50 inspired architecture for feature extraction ($112Gb \to 2.7 Gb$)
  - **PCA/AutoEncoder:** Dimension reduction using PCA ($95\\%$ variance explained) and AutoEncoder (absolute $0.6$ Average Reconstruction loss) ($2.7 Gb \to 0.3 Gb$)

#### Other Team Members:
- Ethan Rajkumar
- Joel Bonnie
- Erhan Javed
- Vivaan Jhaveri 
- Charity Grey

<be>

## Workflow

Chest X-rays, a primary diagnostic tool for identifying thoracic diseases, are the focus of our project, which aims to develop an efficient X-ray representation for automating and benchmarking supervised classification and localization of common thoracic diseases. By leveraging clinical metadata, bounding box annotations, and efficient vector retrieval via Pinecone, we address challenges posed by large-scale datasets (~112k X-rays), annotation constraints, and weak supervision, and build robust classification models using Support Vector Machines (SVM) and Random Forest classifiers.

![image](https://github.com/user-attachments/assets/8085c972-a771-40fa-b14f-ce1f442a45eb)

![image](https://github.com/user-attachments/assets/b1846b59-ede6-4057-9920-cc84416b1d9e)

![image](https://github.com/user-attachments/assets/ca78e5fc-7725-4606-b3f6-262ff0400662)

![image](https://github.com/user-attachments/assets/dbb47c4c-53ab-4a52-98bb-8e5f0efeac0b)

Google slides link: [pdf link](https://drive.google.com/file/d/1daP3G0xtcFt3-vXyv5-XH6YavAcAN3oY/view?usp=sharing)

## Overall metrics for positive classes:
- Overall positive recall: 0.1135
- Overall positive precision: 0.3384
- Overall positive F1 score: 0.1700
- Mean AUC ROC: 0.7242
- Mean Average Precision: 0.1253

## Implications:
1. **Disclaimer:** AIs are note doctors
2. Using algorithms to assist preliminary decisions
3. However, there needs to be studies on the complex of human-robot interaction.
4. Like any other model, the model is vulnerable to concept drift.

---
<br>

### Conda Environments: 
#### Feature Eng
Create the conda environment: 
`conda env create -f environment.yml`

Activate the conda environment: 
`conda activate xray-analysis`
<br>

#### SVC Processing
Create the conda environment: 
`conda env create -f inference_env.yml`

Activate the conda environment: 

`conda activate xray-svc`
