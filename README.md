# Capstone

## Overview
Welcome to my Capstone project! In this project, I have thoroughly cleaned, processed, analyzed, and modeled EEG data to develop a reliable predictive model for diagnosing dementia. By leveraging advanced machine learning techniques, I aim to harness the power of EEG data to accurately identify individuals at risk of dementia. 


## Dataset
This dataset contains the EEG recordings from 88 subjects in total.  
1. Participants: 36 of them were diagnosed with Alzheimer's disease (AD group), 23 were diagnosed with Frontotemporal Dementia (FTD group) and 29 were healthy subjects (CN group). Cognitive and neuropsychological state was evaluated by the international Mini-Mental State Examination (MMSE). The duration of the disease was measured in months and the median value was 25 with IQR range (Q1-Q3) being 24 - 28.5 months. Concerning the AD groups, no dementia-related comorbidities have been reported. 
2. Recordings: Recordings were aquired with 19 scalp electrodes (Fp1, Fp2, F7, F3, Fz, F4, F8, T3, C3, Cz, C4, T4, T5, P3, Pz, P4, T6, O1, and O2) according to the 10-20 international system and 2 reference electrodes (A1 and A2) placed on the mastoids for impendance check, according to the manual of the device. Each recording was performed according to the clinical protocol with participants being in a sitting position having their eyes closed. 
3. Preprocessing: First, a Butterworth band-pass filter 0.5-45 Hz was applied and the signals were re-referenced to A1-A2. Next, the Independent Component Analysis (ICA) method (RunICA algorithm) was performed, transforming the 19 EEG signals to 19 ICA components. 


## Research Question: 
To what extent can the comprehensive analysis of peak frequency, mean frequency, and global power extracted from EEG data provide reliable and discriminative biomarkers for the precise and early detection of dementia (specifically Alzheimers and Frontotemporal Dementia)?

Importance: the importance of this research question lies in the potential for advancing early detection, diagnosis, and understanding of dementia by exploring the role of specific EEG components as reliable biomarkers.
Currently, diagnosing dementia, such as Alzheimers, relies on a combination of clinical assessments, cognitive tests, and neuroimaging techniques. 
However, having reliable biomarkers that can accurately predict the diagnosis of dementia, such as Alzheimer's disease, would greatly enhance early detection and intervention strategies.
By exploring the analysis of specific EEG components as potential biomarkers, this research question addresses the need for non-invasive and accessible diagnostic tools. 


## Dataset and Notebook
The link to the dataset is: https://openneuro.org/datasets/ds004504/versions/1.0.2

The link to the Jupyter Notebook is: https://github.com/Apeksha-Sridhar/Capstone_ML-AI/blob/main/Capstone.ipynb


## Results

### Results from ML models
1. The Decision Tree classifier outperforms the other models in terms of accuracy, precision score, and recall score. The Decision Tree model achieved the highest accuracy, indicating its overall correctness in predicting the disease status. Furthermore, it obtained the highest precision score, demonstrating its ability to correctly classify individuals with dementia. Additionally, the model exhibited the highest recall score, indicating its capability to identify a larger proportion of true positive cases. Based on these observations, the Decision Tree classifier emerges as the clear winner among the models considered in the analysis.
2. The limited number of training samples in EEG data for dementia diagnosis may be a potential reason why random forest models may not outperform decision trees. Random forests typically benefit from a larger amount of training data to effectively capture complex patterns and improve generalization. 

<img width="542" alt="Screen Shot 2023-06-08 at 6 11 27 PM" src="https://github.com/Apeksha-Sridhar/Capstone_ML-AI/assets/122398883/ccccf4f8-9635-416c-8644-d9d0c7965741">

### Results from Convoluted Neural Networks
Despite the longer computational time required, the CNN neural network exhibited exceptional accuracy in diagnosing Alzheimer's disease, Frontotemporal Dementia, and Healthy Aging. The utilization of deep learning techniques enabled the network to effectively extract intricate spatial and temporal features from the EEG data, leading to improved diagnostic accuracy compared to classical ML models.

<img width="403" alt="Screen Shot 2023-06-08 at 6 13 59 PM" src="https://github.com/Apeksha-Sridhar/Capstone_ML-AI/assets/122398883/3bfe035a-3b98-4150-9650-9a733ee682ed">


### Overarching Non-Technical Results
In summary, through the examination of the peak frequency, mean frequency, amd ERPs of EEG components in subjects, we have achieved relatively accurate diagnoses of Dementia and Healthy Aging. Our results demonstrate the effectiveness of employing both classical ML models, particularly decision trees, as well as advanced techniques like CNNs to analyze EEG data and accurately classify neurological conditions. These findings hold promise for enhancing the diagnosis and understanding of these disorders, ultimately contributing to improved patient care and treatment strategies.

## Next Steps
1. Investigation of feature importance: The identification of important features in the random forest model provides valuable insights into the underlying characteristics of neurological conditions. Researchers can delve deeper into these features to understand their physiological or neurological significance, potentially leading to the discovery of new biomarkers or informative features for diagnosis.
2. Validation on larger and diverse datasets: While the current results show promise, validating the models on larger and more diverse datasets is crucial. ML scientists should seek opportunities to access and analyze larger cohorts of EEG data to ensure the generalizability and robustness of their models. This can involve collaborations with research institutions, medical centers, or data sharing initiatives.
3. Translation to clinical practice: To make a real impact, ML scientists should work closely with clinicians, neurologists, and healthcare professionals to validate the models in clinical settings. The field can benefit from collaborative efforts to integrate ML algorithms into existing diagnostic workflows and evaluate their performance in real-world scenarios. This will help in assessing the feasibility, reliability, and practical utility of the developed models.
