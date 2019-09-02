#Random Forest Parameters

x: independent variables of training set. To keep things minimal and simple I am not creating a separate fit method hence the base class            constructor will accept the training set.
y: the corresponding dependent variables necessary for supervised learning (Random forest is a supervised learning technique)
n_trees : number of uncorrelated trees we ensemble to create the random forest.
n_features: the number of features to sample and pass onto each tree, this is where feature bagging happens. It can either be sqrt, log2 or an integer. In case of sqrt, the number of features sampled to each tree is square root of total features and log base 2 of total features in case of log2.
sample_size: the number of rows randomly selected and passed onto each tree. This is usually equal to total number of rows but can be reduced to    increase performance and decrease correlation of trees in some cases (bagging of trees is a completely separate machine learning technique)
depth: depth of each decision tree. Higher depth means more number of splits which increases the over fitting tendency of each tree but since we are aggregating several uncorrelated trees, over fitting of individual trees hardly bothers the whole forest.
min_leaf: minimum number of rows required in a node to cause further split. Lower the min_leaf, higher the depth of the tree