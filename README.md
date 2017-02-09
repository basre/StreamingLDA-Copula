# Streaming-LDA: A Copula-based Approach to Modeling Topic Dependencies in Document Streams
#(C) Copyright 2016, Hesam Amoualian
#hesam.amoualian@imag.fr

#please use this bibtex to cite the paper:
#@inproceedings{amoualian2016kdd, author = {Amoualian, Hesam and Clausel, Marianne and Gaussier, Eric and Amini, Massih-Reza}, title = {Streaming-LDA: A Copula-based Approach to Modeling Topic Dependencies in Document Streams}, booktitle = {Proceedings of the 22nd International Conference on Knowledge Discovery and Data Mining}, series = {SIGKDD}, year = {2016}, isbn = {978-1-4503-4232-2}, location = {San Francisco, California, USA}, pages = {695--704}, numpages = {10}, url = {http://doi.acm.org/10.1145/2939672.2939781}, doi = {10.1145/2939672.2939781}, acmid = {2939781}, publisher = {ACM}, address = {New York, NY, USA}, keywords = {copulas, document streams, latent dirichlet allocation, topic dependencies},}

# References :
# D.M. Blei, A. Ng, M.I. Jordan. Latent Dirichlet Allocation. NIPS, 2002
# G. Heinrich. "Infinite LDA" -- implementing the HDP with minimum code complexity. TN2011/1, www.arbylon.net/publications/ilda.pdf
# Y.W. Teh, M.I. Jordan, M.J. Beal, D.M. Blei. Hierarchical Dirichlet Processes. JASA, 101:1566-1581, 2006

# use python3 for running
# needs to have toy_dataset.text and vocabulary.py in same path
# write Python3 HDPcodeup.py
# You can run the code simply by:
# python Coplda.py [path2train] [Number of topics] [Number of iterations] [Removing stop words] [percent of train documents]
# For instance:
# python Coplda.py toy_dataset.txt 20 50 false 90
# Output:
# 1-cosine(Number of topics).txt   : 1- cosine similarity between topic distributions of two consecutive documents (for example second row number is between doc0 and doc1) (near to zero means more similar)
#lambda(Number of topics).txt   : lambda hyperparameter between topic distributions of two consecutive documents (for example second row number is between doc0 and doc1) (the higher lambda the more similar documents)
#Perplexities(Number of topics).txt  (each row for each iteration)
#topc10words.txt     (top-10 words , each row related to one topic)
