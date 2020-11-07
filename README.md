# GBRL
  The source code in paper "An Alternative GRAPH-BERT-based Deep Reinforcement Learning Framework for Combinatorial Optimization". We propose an alternative reinforcement learning framework based on Graph-Bert, which can be trained by two types of reinforcement learning methods: the policy-based method and the value-function-based method. We take the lead in applying the pretraining-fine tuning paradigm to combinatorial optimization problems.
# The architecture of GBRL
![image](https://github.com/ButterflyCaptain/GBRL/blob/main/%E6%B5%81%E7%A8%8B%E5%9B%BE1.png)
# GRAPH-BERT
  We have applied GRAPH-BERT to the framework as a GNN for data processing, so we used part of the code in "https://github.com/jwzhanggy/Graph-Bert" and referenced it in the paper.
# DataSet
The data set in our experiment, such as VRP, TSP and BA, is the generated data, and the rest data comes from http://snap.stanford.edu/data/index.html.
