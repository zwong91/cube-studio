![image](https://user-images.githubusercontent.com/20157705/204804498-57b85892-88db-4edb-b595-3655e462f042.png)

# 思维导图：

[思维导图地址](https://gitmind.cn/app/docs/ma28m6np)

# mlops一站式平台

登录授权：

 - 多种登录方式的示例，
   - [x] 账号密码，
   - [x] github， 
   - [x] 微信登录，
   - [x] AUTH_OID(支持)，
   - [x] AUTH_LDAP(支持)，
   - [x] AUTH_REMOTE_USER(支持)

 - 多租户
   - [x] rbac权限管理，
   - [x] 项目管理

数据平台：

 - 离线元数据： （通过统一sql多模引擎实现，离线元数据同步，实时元数据查询，sql操作，ddl操作等）
   - [x] 支持仅管理离线元数据
   - [ ] 定时脚本将远程数据库元数据同步到离线元数据内(比如离线同步hive元数据到元数据模块),支持离线元数据模块操作ddl远程数据库(比如增减hive列)
   - [x] 实时查询远程元数据，并支持实时ddl远程数据库。
   - [ ] 离线/实时管理元数据，支持hive/clickhouse/mysql/pg/druid等数据库类型
 - 血缘关系：
   - [ ] 支持表+任务+看板+字段+指标+特征，之间的血缘链路关联，支持离线导入血缘链路管理，前端进行可视化展示
 - 指标管理
   - [x] 指标元数据管理
 - 维表管理： 
   - [x] 支持mysql/postgresql作为维表数据库
 - sql查询引擎： （通过统一sql多模引擎实现，离线元数据同步，实时元数据查询，sql操作，ddl操作等）
   - [x] 支持ck hive，impala，presto，druid等统一查询引擎
   - [x] 支持多任务，查询记录，统一sql解析拦截，异步查询，提供标准sql查询基础类
 - 数据ETL： （通过pipeline编排能力统一对接）
   - [x] 提供标准 任务编排，任务管理模块，任务实例，任务成功率
   - [ ] 支持airflow，ds，az调度器
 - 推送：
   - [ ] 封装推送功能模块：支持邮件，企业微信，钉钉等推送方式
   - [ ] 支持文本，图片，html等推送模式 

AI平台：

 - notebook：
   - [x] 支持基础vscode/jupyter开发环境，支持ssh等功能
   - [x] 大数据版本，数据挖掘版本，深度学习版本
   - [ ] 添加使用示例，比如sparksql/impala/presto/clickhouse/mysql/postgresql等分析建模示例
   - [ ] 添加flink实时分析示例
   - [ ] 添加百G大数据单机数据分析能力Arrow、vaex、duckdb等数据分析能力
 - 镜像仓库管理：
   - [x] 仓库管理
   - [x] 镜像管理
   - [x] 镜像调试
 - 任务模板: 
   - [ ] 添加数据处理模板(导入导出，sqoop，spark等任务类型)
   - [ ] 添加特征处理模板(归一化，转换，...)
   - [ ] 添加模型处理模板(模型压缩，模型转换..)
   - [x] 添加分布式训练模板~~
 - 任务流编排
   - [x] 单任务调试
   - [x] pipeline调试
   - [x] 任务可视化
   - [x] 定时调度
 - 任务流调试： 
   - [x] 去除对kubernetes dashboard的依赖，提供服务支持pod，搜索，日志的查看，删除，执行命令界面
   - [x] kubeflow-pipeline依赖去除
   - [x] 支持任务结果可视化
 - automl：
   - [x] nni超参搜索
   - [ ] ray超参搜索
   - [ ] 特征选择
   - [ ] 框架选择
   - [ ] 模型压缩
 - 特征平台
 - 数据集
   - [x] 数据集存储中心
   - [x] 数据集管理，版本管理等
   - [x] sdk中支持数据自动导入
   - [x] 支持数据集上传
 - 标注平台，集成label studio，与其他模块数据打通
 - 模型管理
   - [x] 模型注册模板
   - [x] 模型下载模板
   - [x] 模型可视化
 - 服务管理：
   - [x] 内部服务
   - [x] 推理服务
     - [x] 添加triton标准镜像
     - [ ] 视频推流sidecar

基础架构能力：

 - 分布式存储方案：
   - [x] 完善juicefs分布式存储方案
   - [ ] 体质sidecar分布式存储挂载，而不是单机挂载
   - [x] 支持alluxio分布式加速
 - 添加边缘集群部署脚本
   - [ ] 添加super edge部署cube studio方案
   - [ ] 添加kube edge部署cube studio方案
 - 私有仓库部署方案：
   - [x] docker-compose部署harbor方案
   
web框架：
- [ ] 支持通用pipeline编排，合并frontend/vison/visonPlus代码
- [x] 通用血缘，支持任务流调试界面，去除kfp依赖~~
- [ ] 中英文支持
- [x] 通用可视化模板~~

# AIHub应用市场 

sdk

- 前后端： （aihub前后端应用）
  - [ ] 适配pc端/手机端
  - [ ] 登录，
  - [ ] 微信打开限制，
  - [ ] 广告sdk，
  - [ ] 功能弹窗，
  - [ ] 大视频文件在线播放，
  - [ ] 支持视频流，
  - [ ] 分享到朋友圈，
  - [ ] 访问统计，
  - [ ] 热度排行，
  - [ ] 智能推荐

- pip包
  - [x] 标准化镜像构建标准
  - [x] 支持生成web服务，微信端服务
  - [x] 支持转训练，注册为job 模板
  - [x] 支持转推理api，批处理，弹性离线推理
  - [x] 支持数据数据集上传和自动加载，与数据集平台对接，外部数据集转内部数据集

算法模型： （自研模型+魔塔模型+hf模型）

- 传统机器学习（jupyter形式）：
  - [x] 基础技能：pandas，matplotlib，pyecharts
  - [x] 关联挖掘：关联分析（Apriori、FP-growth）
  - [x] 分类：决策树（ID3、C4.5、CART）、K最近邻算法(KNN)、kd树、极大似然估计、EM算法、文档分类器，朴素贝叶斯分类器，费舍尔分类器、线性函数、线性回归、正则化、逻辑分类/逻辑回归/一般线性回归、支持向量机SVM、核方法、集成学习（Bagging、Boosting、RF、AdaBoost、GBDT、xgboost）、GBDT算法、XGBOOST算法、CTR/CVR中的FM、FFM算法、LightGBM算法
  - [x] 聚类：层次聚类、BIRCH聚类、k均值聚类、k中心点聚类、DBSCAN密度聚类
  - [x] 图论：最小生成树（MST）的Prim算法和Kruskal算法
  - [ ] 搜索引擎：

- 深度学习模型：
- 大模型数据人

# 社区运营：

 - 组织线下活动，比如社区例会，定期下线见面会
 - 撰写或更新文档，完善github wiki文档，公众号文章，跟踪大厂使用case
 - 知识社区的运营，比如知乎，csdn，B站等，发布帮助视频
 - 帮助新用户，群内答疑
 - 发展社区大使，推广社区
 
