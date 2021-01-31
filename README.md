# Studying-the-Effect-of-Embeddings-on-Named-Entity-Recognition-For-Biomedical-Datasets

This is the sample code for the project conducted for ANLP class at IU Bloomington.

## Abstract
This project is an attempt to study how different embeddings affect the performance of the named entity recognition model. We have ex- perimented with different word embeddings such as Glove (Pennington et al. (2014)), BERT (Devlin et al. (2019)) and PubMed contextual- ized embeddings (Sharma and au2 (2019)) and their combinations. We have used Biomedical datasets to test the named entity recognition ac- curacy. We have reported the testing F1 scores for all embeddings and corresponding datasets. It is interesting to see how some embeddings perform better on medical datasets while others perform poorly.

Biomedical datasets are usually smaller in size and are much harder to annotate. The named entity recognition on these datasets is still an on-going task. Being able to determine which embeddings perform better for such datasets will help improve the results of named entity recognition models for biomedical data. In our outcomes, we have no- ticed that PubMed contextualized embeddings and BERT embeddings give a better performance both individually and in combination.

## Results
The table shows the F1 scores obtained after testing the named entity recognition models. The columns correspond to the different datasets and the rows correspond to the embeddings used to train the models. Most of the datasets are divided into training, development, and testing data. For some datasets, development data was missing, for these datasets, testing data was treated as development data. The size of the training dataset ranged from 891 examples to 5331 examples for individual datasets.

All models were trained for 100 epochs and with a mini batch-size of 128. The initial learning rate was kept as 0.1, the learning rate was adaptable and the trainer decreased the learning rate as needed. The hidden dimension was chosen to be 256. The models were trained using Google Colab Pro GPUs. All models were trained only once because of a lack of resources and time. Ideally, models should have been trained several times and the average results should have been reported. The training and testing result for multiple datasets with PubMed and BERT embeddings could not be computed in the given time-frame of the project due to the lack of proper hardware needed to train them.

Training models with glove and BERT embeddings and their combination were comparatively faster than training models with PubMed embeddings and their combinations. PubMed embeddings are very heavy and take more than twice the time to train.

The best obtained F1 scores, as well as some other interesting F1 scores, have been highlighted in the table. The results clearly show that PubMed embeddings and their combination with BERT embeddings perform well and are worth looking into. For some datasets, BERT embeddings combined with glove embeddings give the best results. PubMed embeddings and BERT embeddings performed well individually as well as in combination with other embeddings. The results also show that training multiple datasets together can be an interesting concept and is certainly something that can be experimented with further upon.

With this project, we set out to get a better understanding of how embeddings affect the performance of named entity recognition models. Our experiments have certainly given us a much clearer idea than before.


## References
Alan Akbik, Duncan Blythe, and Roland Vollgraf. Contextual string embed- dings for sequence labeling. In COLING 2018, 27th International Confer- ence on Computational Linguistics, pages 1638–1649, 2018.

Q. Chen, Y. Peng, and Z. Lu. Biosentvec: creating sentence embeddings for biomedical texts. In 2019 IEEE International Conference on Healthcare Informatics (ICHI), pages 1–5, 2019. doi: 10.1109/ICHI.2019.8904728.

Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. Bert: Pre-training of deep bidirectional transformers for language understand- ing, 2019.
Rezarta Islamaj Doğan, Robert Leaman, and Zhiyong Lu. Ncbi disease corpus: A resource for disease name recognition and concept normal- ization. Journal of Biomedical Informatics, 47:1–10, Feb 2014. doi: 10.1016/j.jbi.2013.12.006.

Alistair E.w. Johnson, Tom J. Pollard, Lu Shen, Li-Wei H. Lehman, Mengling Feng, Mohammad Ghassemi, Benjamin Moody, Peter Szolovits, Leo Anthony Celi, Roger G. Mark, and et al. Mimic-iii, a freely accessible critical care database. Scientific Data, 3(1), 2016. doi: 10.1038/sdata. 2016.35.

Jiao Li, Yueping Sun, Robin J. Johnson, Daniela Sciaky, Chih-Hsuan Wei, Robert Leaman, Allan Peter Davis, Carolyn J. Mattingly, Thomas C. Wiegers, Zhiyong Lu, and et al. Biocreative v cdr task corpus: a resource for chemical disease relation extraction. Database, 2016, May 2016. doi: 10.1093/database/baw068.

Jeffrey Pennington, Richard Socher, and Christopher D. Manning. Glove: Global vectors for word representation. In Empirical Methods in Natural Language Processing (EMNLP), pages 1532–1543, 2014. URL http:// www.aclweb.org/anthology/D14-1162.

Matthew E. Peters, Mark Neumann, Mohit Iyyer, Matt Gardner, Christo- pher Clark, Kenton Lee, and Luke Zettlemoyer. Deep contextualized word representations. In Proc. of NAACL, 2018.

Sampo Pyysalo, Filip Ginter, Juho Heimonen, Jari Björne, Jorma Boberg, Jouni Järvinen, and Tapio Salakoski. Bioinfer: a corpus for information extraction in the biomedical domain. BMC Bioinformatics, 8(1), 2007. doi: 10.1186/1471-2105-8-50.

Sampo Pyysalo, Tomoko Ohta, and Sophia Ananiadou. Overview of the cancer genetics (CG) task of BioNLP shared task 2013. In Proceedings of the BioNLP Shared Task 2013 Workshop, pages 58–66, Sofia, Bulgaria, August 2013. Association for Computational Linguistics. URL https: //www.aclweb.org/anthology/W13-2008.
C. Ronran and S. Lee. Effect of character and word features in bidirectional lstm-crf for ner. In 2020 IEEE International Conference on Big Data and Smart Computing (BigComp), pages 613–616, 2020. doi: 10.1109/ BigComp48618.2020.00132.

A. Shaik and W. Jin. Biomedical semantic embeddings: Using hybrid sen- tences to construct biomedical word embeddings and its applications. In 2019 IEEE International Conference on Healthcare Informatics (ICHI), pages 1–9, 2019. doi: 10.1109/ICHI.2019.8904533.

Shreyas Sharma and Ron Daniel Jr au2. Bioflair: Pretrained pooled contex- tualized embeddings for biomedical sequence labeling tasks, 2019.

J. Thadajarassiri, C. Sen, T. Hartvigsen, X. Kong, and E. Rundensteiner. Comparing general and locally-learned word embeddings for clinical text mining. In 2019 IEEE EMBS International Conference on Biomedi- cal Health Informatics (BHI), pages 1–4, 2019. doi: 10.1109/BHI.2019. 8834672.

Erik F. Tjong Kim Sang and Fien De Meulder. Introduction to the conll- 2003 shared task: Language-independent named entity recognition. In Proceedings of the Seventh Conference on Natural Language Learning at HLT-NAACL 2003 - Volume 4, CONLL ’03, page 142–147, USA, 2003. Association for Computational Linguistics. doi: 10.3115/1119176.1119195. URL https://doi.org/10.3115/1119176.1119195.
