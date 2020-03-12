# Xgboost_training_model
## Xgbosst 参数

 - 'booster':'gbtree'。用梯度提升的决策树进行节点分裂
 - 'objective': 'multi:softmax', 多分类的问题。损失函数，有分类，有回归
 - 'num_class':10, 类别数，与 multisoftmax 并用
 - 'gamma':损失下降多少才进行分裂
 - 'max_depth':12, 构建树的深度，越大越容易过拟合
 - 'lambda':2, 控制模型复杂度的权重值的L2正则化项参数，参数越大，模型越不容易过拟合。
 - 'subsample':0.7, 随机采样训练样本（对样本采样）
 - 'colsample_bytree':0.7, 生成树时进行的列采样（对特征采样）
 - 'min_child_weight':3, 孩子节点中最小的样本权重和。如果一个叶子节点的样本权重和小于min_child_weight则拆分过程结束
 - 'silent':0 ,设置成1则没有运行信息输出，最好是设置为0.
 - 'eta': 0.007, 如同学习率，串行添加树，新加进来的树贡献占比多少。经验上讲增大树的数量，降低学习率
 - 'seed':1000,
 - 'nthread':7, cpu 线程数

## Xgbosst 参数调节

 - Step 1: 选择一组初始参数
 - Step 2: 改变 max_depth 和 min_child_weight.
 - Step 3: 调节 gamma 降低模型过拟合风险.
 - Step 4: 调节 subsample 和 colsample_bytree 改变数据采样策略.
 - Step 5: 调节学习率 eta.
