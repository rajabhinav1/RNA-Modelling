# RNA-Modelling
Stanford Ribonanza RNA Folding

Description
Ribonucleic acid (RNA) is essential for most biological functions. A better understanding of how to manipulate RNA could help usher in an age of programmable medicine, including first cures for pancreatic cancer and Alzheimer’s disease as well as much-needed antibiotics and new biotechnology approaches for climate change. But first, researchers must better understand each RNA molecule's structure, an ideal problem for data science.

Recent efforts to predict RNA structure have run into a number of challenges: (1) a paucity of training data, (2) lack of intellectual and computational power, and (3) difficulties in rigorously splitting training and test data. Can a Kaggle competition close these gaps?

Towards sourcing a large and diverse collection of RNA molecules for data acquisition, the host Das laboratory brings together scientists and gamers to solve puzzles and invent medicine in the Eterna project. The Eterna community has previously unlocked new scientific principles, designed thermodynamically-optimized riboswitches, and revealed RNA degradation patterns for improving the shelf life of mRNA vaccines, which formed the basis of the Kaggle OpenVaccine challenge. Now the Eterna project is creating diverse sequences that are predicted to form complex structures.

The data for this new Ribonanza competition are experimental measurements of the chemical reactivity at each position of an RNA molecule. These data are exquisitely sensitive to the structure – or multiple structures – that each RNA forms in the test tube. An algorithm that could perfectly predict these chemical reactivities would need to have an implicit ‘understanding’ of RNA structure to do so. Such an oracle could be then utilized to predictively model structures of novel RNA molecules. As in the OpenVaccine competition, the majority of the private leaderboard data will be collected in parallel with your prediction efforts -- no one will know the answers until the competition closes!

To reiterate the potential impact of your participation, an accurate model that solves the RNA structure prediction problem could be a game changer for medical researchers who are trying to identify unique RNA-based drug targets in the many bacterial, viral, neurological, and cancer genes that remain undruggable at the protein level. In addition, accurate RNA structure prediction is needed to predictively design RNA-based medicines such as mRNA vaccines and CRISPR gene therapeutics that promise to treat nearly all human disease. More than its medical implications, RNA molecules underlie and can even dominate core biological processes for all of life, including the very first forms of life on Earth and the plants and marine organisms that fix most of the carbon on our planet now. A full understanding of life requires a full, predictive understanding of RNA.

In addition to being made available as open source code for the entire science and medicine communities, winners’ innovations will be featured in a keynote talk by Rhiju Das at the flagship conference in machine learning in structure biology at NeurIPS in December 2023.

         

Evaluation
Submissions are scored using MAE, mean absolute error:


where 
 is the number of scored ground truth values, and 
 and 
 are the actual and predicted values, respectively. The 
 values will be clipped between 0 and 1 before calculating MAE, that is:


where 
 are the raw data values.

From the Data page: At each position of each RNA sequence, there will be two ground truth values, corresponding to reactivity determined from two kinds of chemical mapping experiments, DMS_MaP and 2A3_MaP.

Submission File
For each sequence in the test set, you must predict target reactivities for each sequence position id, two per row. If the sum of the lengths of all 1,343,824 sequences in the test set is 269,796,671, then you should make 2 
 269,796,670 = 539,593,340 predictions.

id,reactivity_DMS_MaP,reactivity_2A3_MaP
0,0.1,0.3
1,0.3,0.2
2,0.5,0.4
etc.


https://www.kaggle.com/competitions/stanford-ribonanza-rna-folding
https://www.kaggle.com/code/abhinavraj111/basic-xg-boost-for-rna-computing
