# NR-Profiler
**Profiling prediction of nuclear receptor modulators with multi-task deep learning methods: toward the virtual assay.** Jiye Wang, Chaofeng Lou, Guixia Liu, Weihua Li, Zengrui Wu and Yun Tang. Manuscript to be submitted.

Nuclear receptors (NRs) are ligand-activated transcription factors, which constitute one of the most important targets for drug discovery. Current computational strategies mainly focus on a single target, and the transfer of learned knowledge among NRs was not considered yet. Herein we proposed a novel computational framework named NR-Profiler for prediction of potential NR modulators with high affinity and specificity. At first, we built a comprehensive NR data set including 42,684 interactions to connect 42 NRs and 31,033 compounds. Then, we used multi-task deep neural network (MT-DNN) and multi-task graph convolutional neural network (MT-GCN) architectures to construct multi-task multi-classification models. To improve the predictive capability and robustness, we built a consensus model with an AUC (area under curve) = 0.883. Compared with conventional machine learning and structure-based approaches, the consensus model showed better performance in external validation. Using this consensus model, we demonstrated the practical value of NR-Profiler in virtual screening for NRs. In addition, we designed a selectivity score to quantitatively measure the specificity of NR modulators. Finally, we developed a freely available standalone software for users to make profiling predictions for their compounds of interest. In summary, our NR-Profiler provides a useful tool for NR profiling prediction and is expected to facilitate NR-based drug discovery.

![deepNR-workflow_01](https://user-images.githubusercontent.com/46025194/162143217-77029496-9325-4fd3-bf2f-eb1c36c33517.png)

Figure 1. The schematic diagram of NR-Profiler, including four parts: (a) construction of nuclear receptors data set based on large-scale bioactivity data, (b) the multi-task deep neural network (MT-DNN) architecture with the molecular fingerprint as input, (c) the multi-task graph convolutional neural network (MT-GCN) architecture with the molecular graph as input, and (d) model application in nuclear receptor profiling prediction of each compound.

# Dataset
All the data is available in the 'dataset.zip' folder, including:
1. The NR-2019 dataset
2. The NR-2021 dataset
3. The Total dataset

# Software
We developed a standalone software called NR-Profiler via the python package Tkinter for the prediction of novel potential NR modulators (**Figure 2**). The consensus model was encapsulated in this software. With the software, researchers can input their in-house data and then obtain predictive lists. The general process is as follows. Firstly, users can choose two types, including basic and advanced predictions. Then, users can make predictions by simply inputting the canonical SMILES format of the compound. Finally, users can select the output path of the prediction results and start to predict. The predicted results of NR-Profiler are saved in a CSV format file. Users can choose these interactions with label = 2 (equivalent to “B”) and lower selectivity score S for further experimental validation. It is estimated that the time required for the software to predict a compound is about 7 seconds on the Intel (R) Core (TM) i5-7500 CPU (8 GB system memory). As the number of predicted compounds increases, the time it takes to predict will increase (100 molecules in about 1 minute). It depends on the hardware configuration of the computer. 

The NR-Profiler software (v1.0) is freely available at https://www.amazon.com/clouddrive/share/CYRXxdJr8q3J0QBDm0L3MG65erCingdDLAjRsC6Xanu for Windows operating system.

![微信图片_20220331141025](https://user-images.githubusercontent.com/46025194/162142469-8d79ac65-2ad2-46dc-90ad-c82c0d4550c1.png)

Figure 2. The software interface of NR-Profiler. Users can choose two types, including basic and advanced predictions. The basic prediction type is to predict the nuclear receptor profiling for single-molecule. The advanced prediction type is to predict the nuclear receptor profiling for thousands of compounds.

# Guide
Users can choose two types, including basic and advanced predictions. Then, users can make predictions by simply inputting canonical SMILES format of the compound. When users select the advanced prediction type, the input file must be a CSV format file and use “smiles” as the header. Finally, users can select the output path of the prediction results and start to predict. The predicted results are saved in a CSV format file. Users can choose these interactions with label = 2 (equivalent to “Binder”) for further experimental validation. It is estimated that the time required for the software to predict a compound is about 7 seconds on the Intel (R) Core (TM) i5-7500 CPU (8 GB system memory). As the number of predicted compounds increases, the time it takes to predict will increase (100 molecules in about 1 minute). It depends on the hardware configuration of the computer.

# Developer Information
Maintainer: Dr. Lou, Dr. Wang, Dr. Wu and Professor Tang

Contact US: ytang234@ecust.edu.cn

Laboratory of Molecular Modeling and Design

School of Pharmacy, East China University of Science and Technology
