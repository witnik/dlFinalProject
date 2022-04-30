# dlFinalProject

de novo drug exploration with sandwich smile transformer  

# Introduction
Machine learning is showing promise in de novo drug development virtual screening. Molecular fingerprints are computed using deep learning methods, mapping molecules to a sparse discrete space, then using the multilayer perceptron classifiers and regressors to predict molecular properties pertaining to drug applications. However, these algorithms perform poorly for shallow prediction models or small datasets. SMILES Transformer attempts to improve upon this deficit by learning molecular fingerprints through unsupervised pre-training of the sequence-to-sequence language model using a huge corpus of SMILES, a text representation system for molecules. To improve upon this baseline model, we hypothesize that the specific rearrangement of the transformer sublayers, called sandwich transformers, could potentially enhance the encoding of the molecules. We trained and tested the same MLP for three unique classification tasks on 3 respective drug target datasets on the SMILES transformer versus six different models with unique rearrangements of the transformer sublayers: coefficients-1,2,3 for encoder and decoder layers, respectively.  The sandwich transformer decoder models performed better than encoder models in our experiments, the sandwich transformer decoder  models made our results display a modest improvement in two out of three of the datasets, proving the effectiveness of the sandwich transformer.

## Instructions on running the project
The dataset is too large for Github. You can download it here with this URL: https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/releases/chembl_24/archived/. Download file 'chembl_24_chemreps.txt.gz' and then process it to get the dataset using ‘data_process' notebook.
Directly run through the ‘Sandwich_Transformer’ notebook to train the transformer model and using ‘eval’ notebook to get the final results.

reference:

https://github.com/EBjerrum/SMILES-enumeration
https://pytorch.org/docs/stable/_modules/torch/nn/modules/transformer.html#Transformer
