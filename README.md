# PoPETS2024-submission274

This GitHub repository contains code of the #275 submission to PoPETS2024.4 (4-th issue)

This repository contains two main directories : 

1) FHE-Fairness-awareFL : This directory contains the implementation of the specified homomorphic aggregation at section 6.

     As specified in the submission, this implementation is composed of two modules.
             -A tensorflow v2 module that represents local training of the clients
             -A lattigo module representing the server's homomorphic (With CKKS) fairness-aware aggregation.
     An intermediate directory "SharedFiles" serves to simulate the network, where clients write their updated models, and the server reads, encrypts then aggregates them.  

    Dependencies :
       Lattigo homomorphic library.
       Tensorflow (lattest version).


3) Enhanced_MIA : This directory contains the implementation of the enhanced membership inference attacks using prior knowledge of the target classifer's fairness level (a fairness metric evaluation). It impelemnts the FairGAN architecture to generate parametrically biased data. This data later serves as input to train, and perform inferences for three shadow models. Finally, an attack classifier is trained to predict the membership status of a data-record.
 
    Dependencies :
      Tensorflow.
      Adverserial-Robustness-Toolbox.


*****************Datasets***********************
Three datasets are required to evaluate these experiments : 
1) Adult-Census-Income
2) Compas-Risk-Recidivism
3) FairFace


       
