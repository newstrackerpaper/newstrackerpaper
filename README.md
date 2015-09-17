For [1], this repository contains (references to) the implementation, result files of the empirical evaluation and annotated ground truth. 

The artifact io.github.k3nn 0.01 (Maven central or working version in https://github.com/k3nn/k3nn) contains the core implementation for 3NN clustering and relevance ranking against recent salient information. The components are generic to allow reuse in projects that use different data types.

The github repository https://github.com/k3nn/topictracking contains a maven project with the code we used to process the 2013 KBA Streaming Corpus to produce the published results.

In this repository are the TREC results files and the annotated ground truth. The zipped archives contain a sweep of parameter settings. There are four versions:
<ul>
<li>main: uses self extracted titles, cosine similarity over binary word vectors (no IDF) and estimates the amount of previously seen information by the number of 2-word combinations.
<li>no-titles: titles were used to cluster news articles, but no titles were returned as result.
<li>unigram: previously seen information is estimated over unigrams
<li>idf: cosine similarity is computed usig tf-idf.
</ul>

The ground truth contains a pool file with all retrieved sentences and a matching file that has te annotated labels for scoring using the offical TREC eval tool.

[1] Jeroen B.P. Vuurens, Arjen P. de Vries, Roi Blanco, Peter Mika, "Online News Tracking for Ad-Hoc Information Needs", in Proceedings of ICTIR 2015. 
