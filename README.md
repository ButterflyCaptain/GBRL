# GBRL
  The source code in paper "An Alternative GRAPH-BERT-based Deep Reinforcement Learning Framework for Combinatorial Optimization". We propose an alternative reinforcement learning framework based on Graph-Bert, which can be trained by two types of reinforcement learning methods: the policy-based method and the value-function-based method. We take the lead in applying the pretraining-fine tuning paradigm to combinatorial optimization problems.
# The architecture of GBRL
![image](https://github.com/ButterflyCaptain/GBRL/blob/main/%E6%B5%81%E7%A8%8B%E5%9B%BE1.png)
# GRAPH-BERT
  We have applied GRAPH-BERT to the framework as a GNN for data processing, so we used part of the code in "https://github.com/jwzhanggy/Graph-Bert" and referenced it in the paper.
# DataSet
The data set in our experiment, such as VRP, TSP and BA, is the generated data, and the rest data comes from http://snap.stanford.edu/data/index.html.
# How to run
# Data generation
python create_data.py --problem all --name validation --seed 

python create_data.py --problem all --name test --seed 
# GBRL_R 
We take generating data TSP50 as an example to demonstrate the training method.

python R_train.py --graph_size 50 --run_name 'tsp50' --dataset data/tsp/tsp50_training_seed1.pkl

python R_run.py --graph_size 50 --run_name 'tsp50' --dataset data/tsp/tsp50_validation_seed2.pkl
# GBRL_Q 
python Q_train.py --graph_size 50 --run_name 'tsp50' --dataset data/tsp/tsp50_training_seed1.pkl

python Q_run.py --graph_size 50 --run_name 'tsp50' --dataset data/tsp/tsp50_validation_seed2.pkl
