## 游戏对局数据获取

#### 国服：腾讯游戏平台非官方API - http://www.games-cube.com/

|游戏版本|游戏模式|艾欧尼亚|诺克萨斯|黑色玫瑰|扭曲丛林|合计|数据预处理|
| ------- | ------------ | -------- | -------- | -------- | -------- | -------- | ------------------------------ |
|6.23|极地大乱斗|108155|67753|-|209911|385819|去除未满级对局|
|6.24|极地大乱斗|187479|130584|-|191964|510027|去除未满级对局<br>去除战绩异常对局|
|7.4|无限乱斗|10335|-|7681|18587|36603|去除战绩异常对局|

#### 外服：Riot开发者平台API - https://developer.riotgames.com/

|游戏版本|游戏模式|美服|西欧服|韩服|合计|
| ------- | ------------ | -------- | -------- | -------- | -------- |
|7.6|排位赛(单排/双排)|89689|100506|116531|306726|
|7.6|匹配模式|79682|75069|63358|218109|
|7.6|极地大乱斗|58243|57746|49180|165169|
|7.7|排位赛(单排/双排)|221922|209570|307744|739236|
|7.7|排位赛(灵活组排)|44900|49177|74948|169025|
|7.7|匹配模式|268090|233730|191378|693198|
|7.7|极地大乱斗|152789|121002|111397|385188|
|7.7|峡谷大乱斗|39235|26391|20910|86536|
|7.8|极地大乱斗|278343|225338|257006|760687|
|7.8|魄罗大乱斗|113635|83110|37470|234215|

## 游戏对局胜负预测

### 根据双方英雄阵容，预测获胜方的准确率（%）

|游戏版本|游戏模式|随机森林|AdaBoost|XGBoost|支持向量机|Logistic回归|神经网络|
| ------ | ------------ | -------- | -------- | -------- | -------- | -------- | -------- |
|6.23|极地大乱斗| 66.3 | 67.9 | 68.0 | 68.0 | 67.9 | **69.2** |
|6.24|极地大乱斗| 66.0 | 67.3 | 67.5 | 67.3 | 67.3 | **68.6** |
|7.6|极地大乱斗| 65.0 | 66.8 | 66.4 | 66.7 | 66.7 | **67.6** |
|7.7|极地大乱斗| 65.2 | 66.6 | 66.7 | 66.6 | 66.6 | **67.7** |
|7.8|极地大乱斗| 66.0 | 67.1 | 67.6 | 67.2 | 67.1 | **68.4** |
|7.8|魄罗大乱斗| 63.0 | 64.2 | 64.1 | 64.3 | 64.2 | **64.8** |
|7.4|无限乱斗| 62.1 | 64.4 | 63.3 | 64.1 | 64.2 | **64.5** |
|7.7|峡谷大乱斗| 56.9 | 58.5 | 57.9 | 58.3 | 58.5 | 58.7 |
|7.6|匹配模式| 53.7 | 55.1 | 54.8 | 54.7 | 55.1 | 55.1 |
|7.7|匹配模式| - | - | - | - | 56.0 | 56.2 |
|7.6|排位赛(单排/双排)| 53.9 | 54.8 | 54.4 | 54.8 | 54.8 | 54.8 |
|7.7|排位赛(单排/双排)| - | - | - | - | 54.8 | 55.1 |
|7.7|排位赛(灵活组排)| - | - | - | - | 54.6 | 54.7 |

### 只根据本方英雄阵容，预测本方能否获胜的准确率（%）				

|游戏版本|游戏模式|随机森林|AdaBoost|XGBoost|支持向量机|Logistic回归|神经网络|
| ------ | ------------ | -------- | -------- | -------- | -------- | -------- | -------- |
|6.23|极地大乱斗| 59.8 | 62.2 | 62.3 | 62.3 | 62.2 | **62.9** |
|6.24|极地大乱斗| 59.4 | 61.8 | 62.0 | 61.9 | 61.8 | **62.3** |
|7.6|极地大乱斗| 59.4 | 61.6 | 61.7 | 61.6 | 61.6 | **62.3** |
|7.7|极地大乱斗| 59.3 | 61.6 | 61.7 | 61.7 | 61.6 | **62.2** |
|7.8|极地大乱斗| - | 61.8 | 62.1 | 61.9 | 61.8 | **62.4** |
|7.4|无限乱斗| 58.5 | 60.5 | 60.0 | 60.6 | 60.6 | **60.6** |
|7.8|魄罗大乱斗| 56.5 | 59.1 | 59.0 | 59.1 | 59.1 | 59.4 |
|7.7|峡谷大乱斗| 54.0 | 56.0 | 55.6 | 56.0 | 56.0 | 56.5 |
|7.6|匹配模式| 51.8 | 53.8 | 53.7 | 53.6 | 53.8 | 53.9 |
|7.7|匹配模式| - | - | - | - | 54.1 | 54.5 |
|7.6|排位赛(单排/双排)| 51.2 | 53.4 | 53.1 | 53.4 | 53.5 | 53.5 |
|7.7|排位赛(单排/双排)| - | - | - | - | 53.5 | 53.7 |
|7.7|排位赛(灵活组排)| - | - | - | - | 53.4 | 53.4 |
