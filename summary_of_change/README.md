## Summary of Change
In this paper, we have made significant revisions and added substantial analysis for the proposed framework. We summarize the change in this paper comparing to the ICDM version as follows.  
* Firstly, we have almost completely revised the optimization algorithm, which improves the efficiency and stability of the proposed framework. In particular, we have gained deeper understandings of the properties of the optimization problem (e.g., Lemma 1, Lemma 2, and Section 4.2, 4.3, 4.4.1, 4.6), which leads to solving the optimization problem more efficiently and stably than the projection method in the ICDM version. Moreover, our theoretical analysis shows that the objective function can be rewritten as the sum of many quadratic functions that share a Hessian matrix, which allows us to modify the d.c. algorithm [13] (please see the pape for the reference) to optimize these quadratic functions all at once. 
* Secondly, as a consequence of improved stability, the proposed framework with the new optimization method can learn a good graph even without dataset-specific parameter tuning, which will be reported in the Appendix. 
* Thirdly, we theoretically show that the time complexity of the new optimization approach is basically linear in the number of edges in the multi-view graphs or in the number of nodes in the kNN graphs, even though exactly solving the problem is NP-hard. 
* Fourthly, we introduce multi-view dense representation to replace the sparse matrix used in the ICDM version that consumes three times larger memory and is less efficient. And a graph normalization method is added to the two graph fusion algorithms (SGF and DGF), which improves the performance of clustering. 
* Fifthly, we introduce view-specific weights for every view in our framework so that users can force the unified graph closer to the important views. 
* Last but not least, the experimental section is substantially extended, where more benchmark datasets are used and more experimental comparison and analysis are provided, which further demonstrate the effectiveness and robustness of the proposed framework. 