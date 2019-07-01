# IFLYTEK AI Marketing Algorithm Competition


## 竞赛背景
讯飞AI营销云在高速发展的同时，积累了海量的广告数据和用户数据，如何有效利用这些数据去预测用户的广告点击概率，是大数据应用在精准营销中的关键问题，也是所有智能营销平台必须具备的核心技术。

本次大赛提供了讯飞AI营销云的海量广告投放数据，参赛选手通过人工智能技术构建预测模型预估用户的广告点击概率，即给定广告点击相关的广告、媒体、用户、上下文内容等信息的条件下预测广告点击概率。希望通过本次大赛挖掘AI营销算法领域的顶尖人才，共同推动AI营销的技术革新。


## 主办方
讯飞AI营销云隶属于科大讯飞股份有限公司， 基于深耕多年的人工智能技术和大数据积累，赋予营销智慧创新的大脑，以健全的产品矩阵和全方位的服务，帮助广告主用AI实
现营销效能的全面提升，打造数字营销新生态。


## 任务
讯飞AI营销广告点击率预估，预测广告被点击的概率。


## 数据
数据集包括两个部分：
1. round1_iflyad_train.txt 训练集，每一行数据为一个样本，可分为5类数据，包含基础广告投放数据、广告素材信息、媒体信息、用户信息和上下文信息，共1001650条数据。其中‘click’字段为要预测的标签，其它34个字段为特征字段。
2. round1_iflyad_test_feature.txt 测试集，共40024条数据，与训练集文件相比，测试集文件无‘click’字段，其它字段同训练集。

出于数据安全保证的考虑，所有数据均为脱敏处理后的数据。数据集提供了若干天的样本，最后一天数据构成了测试集，其余日期的数据作为训练数据。

### 基本数据:

字段 | 解释
---- | ----
instance_id | 样本id
click | 是否点击


### 广告信息:

广告 | 解释
---- | ----
adid | 广告id
adver_id | 广告主id
orderid | 订单id
advert_industry_inner | 广告主行业
advert_name | 广告主名称
campaign_id | 活动id
creative_id | 创意id
creative_type | 创意类型
creative_tp_dnf | 样式定向id
creative_has_deeplink | 相应素材是否有deeplink(Boolean)
creative_is_jump | 是否是落地页跳转(Boolean) 
creative is download | 是否是落地页下载(Boolean) 
creative_is_js | 是否为js素材(Boolean) 
creative is_ voiced | 是否是语音广告(Boolean) 
creative width | 创意宽
creative_height | 创意高


### 媒体信息:

字段 | 解释
---- | ----
app_cate_id | app分类
f-channel | 一级频道
app_id | 媒体id
inner_slot_id | 媒体广告位
app_paid | app是否付费


### 用户信息：

字段 | 解释
---- | ----
user_tags | 用户标签信息，以逗号分隔


### 上下文信息：

字段 | 解释
---- | ----
city | 城市
carrier | 运行商
time | 时间戳
province | 省份
nnt | 联网类型
deytype | 设备类型
os_name | 操作系统名称操作
osv | 系统版本
os | 操作系统
make | 品牌（例如: apple）
model | 机型（例如:"iphone"）


补充说明：
1.advert_industry_inner字段数据样例为102400_102401，“102400(前者)”表示广告主一级行业标签id，“102401(后者)”表示广告主二级行业id，如“教育_培训”
2.time字段脱敏后为有序排列，且时间间隔和与真实时间对应。


## 评分算法


