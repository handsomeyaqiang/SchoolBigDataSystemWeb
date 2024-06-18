# SchoolBigDataSystemWeb

#### 介绍
本项目是根据大数据分析后的结果利用echarts进行设计并数据结果可视化展示的Javaweb项目,分析项目在[SchoolBigDataAnalysis](https://github.com/handsomeyaqiang/SchoolBigDataAnalysis)

#### 软件架构
IDEA+Maven
#### 系统结构设计 
图中是对系统的结构设计，主要包括以下几个部分：(1)对分析数据的预处理；(2)对学生的行为聚类分析；(3)对学生的行为关联分析；(4)学生画像构建部分；(5)消费和借阅榜单统计部分；(6)可视化展示部分。

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095237_a4b07cea_1800784.png "系统结构.png")

### 系统流程图 
本系统主要流程是将学生的分析数据利用Sqoop工具从传统数据仓库中移到大数据的Hive数据仓库中，利用SparkSQL集成HiveSQL对数据进行预处理和统计、对处理好的数据进行学生行为聚类分析、学生行为关联分析、构建学生画像、统计分析实现榜单功能、最后对结果利用Echarts进行可视化展示，主要系统流程如图所示：

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095249_3d7e2fc7_1800784.png "系统流程.png")

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095835_78207d4d_1800784.png "2019-05-28_095715.png")

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095851_7eda28a7_1800784.png "2019-05-28_095743.png")

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095902_ed05ba20_1800784.png "搜狗截图20190528095613.png")
### 学生消费榜单
学生消费榜单主要包括一卡通学院消费榜、一卡通星座消费榜、一卡通省份消费榜。

1)一卡通学院消费榜
用户可以选择不同的年级，查看该年级下面的所有学院的消费排名情况，也可以查看所有年级下的学院总消费排行榜。用户进入首页后，点击一卡通消费学院榜，系统会展示出所有年级的学院总消费排行榜；当用户选择年级下拉框里的某个年级后，点击榜单查询，系统会展示出用户选择的年级下面的所有学院的消费排行榜。

2)一卡通星座消费榜
用户可以选择不同的年级，查看某个年级下的学生所属星座的星座消费榜单，也可以查看所有年级下星座总消费排行榜。用户进入首页后，点击一卡通消费星座榜，系统会在页面展示出所有年级的学院星座总排行榜；用户选择年级下拉框中的某个年级后，点击榜单查询，系统会在页面展示已选择的年级下学生星座消费排行情况。

3)一卡通省份消费榜
用户可以选择不同的年级，查看某个年级中的学生所在地区的省份消费排行榜，用户进入首页后，点击一卡通消费省份榜，系统会默认展示所有年级下的学生所属地区的省份消费排行榜，用户选择年级下拉框中的某个年级后，点击榜单查询，系统会在页面展示出该年级下的学生所在地区省份消费榜。
### 学生借阅榜单
学生借阅榜单主要包括图书借阅榜、书籍常阅榜、星座借阅榜、学院借阅榜。

1)图书借阅榜
该模块实现了用户能够查看年级、学院中学生个人的借阅排行情况。用户可以在进入首页后，点击图书借阅榜，系统会默认在页面中展示所有年级下所有学院学生的个人图书借阅排名情况，包括排名信息、脱敏学号信息、脱敏姓名信息、学院信息、借阅数量信息；用户可以选择不同的年级和学院来查询某个年级下的某个学院的个人图书借阅排行情况；用户还可以在输入框中输入自己的学号来查看自己在所有年级中的借阅排名、在自己所在年级中的借阅排名情况。

2)书籍常阅榜
该功能实现了用户可以查看年级、学院中哪些图书经常会被借阅。用户可以进入首页后，点击书籍常阅榜，系统会默认在页面中展示所有年级、所有学院中学生所借阅的书籍的排行榜单并展示，展示的榜单信息有排名、书名、类别、借阅数量信息；用户可以选择不同年级和学院的查询条件，点击榜单查询后，系统展示某年级的学院中学生借阅的书籍排行榜单在页面中。

3)星座借阅榜
用户可以根据年级来查看该年级学生中不同星座的借阅排行情况。用户点击图书借阅星座榜后，系统会在页面展示出本校所有年级学生中不同星座的借阅情况；用户也可以选择某个年级，查看该年级的学生星座借阅榜单。

4)学院借阅榜
用户可以根据年级来查看该年级下的不同学院的图书借阅情况。用户进入首页后点击图书借阅学院榜，系统会在页面中展示本校所有年级下的不同学院图书借阅排行榜；用户在年级下拉框中选择不同年级，点击榜单查询，系统会展示出该年级下有学院的图书借阅情况。
### 学生画像展示
学生画像展示部分主要包括学生行为特征画像展示和学生图书借阅特点画像。

1)学生行为特征画像展示
用户可以根据学生行为特征画像明显看出不同学生的在校行为特征。用户进入首页后，点击舆情中的消费大数据平台，系统会跳转到该页面，用户可以在输入框中输入要查看的学号信息，点击查询按钮，系统会去请求该学生的行为特征画像信息并展示，用户看到不同行为特征展示的大小会有不同，将鼠标悬停在某个画像标签上，页面会展示该画像标签的权重大小。

2)学生图书借阅特点画像
用户可以根据学生图书借阅特点画像很明显看出学生的借书特点。用户进入首页后，点击舆情中的图书门禁大数据平台，系统会跳转至该页面，用户可以在输入框中输入要查看的学号信息，点击查询按钮，系统会在页面中展示出该学号对应的学生图书借阅特点画像信息。
### 省份消费地图
省份消费地图模块中，用户可以查看某个年级的学生所属地区的省份排行榜以及不同省份的消费情况对应到省份地图中，以此来查看学校不同年级中来自不同地区的学生消费情况。用户进入消费大数据平台页面后，用户可以在该页面选择要查看的某个年级的学生省份消费情况，点击查询按钮后，系统会将该年级学生中所属地区的省份排行及消费情况进行展示，可以明显出来自不同省份的学生消费情况。
### 个人消费统计展示
用户可以根据学号查找个人的消费金额统计和个人消费频次统计详情，用户点击首页的舆情中的消费大数据平台，用户在给页面的输入框中输入自己要查找的学号信息，点击查询按钮后，系统会将该学号在校的消费金额统计详情和不同消费类型的消费频次统计信息进行展示，消费金额统计详情包括早餐消费金额、午餐消费金额、晚餐消费金额和总消费金额，消费频次统计包含早餐频次、午餐频次、晚餐频次、总消费频次。
### 个人借阅统计展示
个人借阅统计展示了学生个人的借阅书籍的统计。用户进入首页点击舆情中的图书门禁大数据平台后，在输入框中输入要查找的学号信息并点击查询按钮，系统会展示该学号的书籍借阅统计值，包括借阅次数和借阅总数信息。
### 学生行为特征占比展示
学生行为特征占比展示部分包括学生消费水平占比、生活规律占比、学习强度占比。

1)消费水平群体占比
用户可以查看每个年级中的学生消费水平群体的占比情况，以此分析判断出该年级学生中的主流消费群体。用户在学生消费大数据平台页面中，选择年级下拉框中的某个要查找的年级，点击查询按钮，系统会在页面展示该年级中不同消费水平的占比数据，主要包括四种消费群体：(1)中等消费、消费稳定；(2)低消费、消费稳定；(3)偏低消费、校外消费、校外居住；(4)高消费、消费稳定。

2)生活规律群体占比
用户可以查看每个年级中的学生生活规律群体的占比情况，以此判断出该年级中学生的生活规律情况如何。用户进入学生消费大数据平台页面后，选择下拉框中的要查找的年级，点击查询按钮，系统会根据展示出该年级去请求此年级的生活规律群体占比值，主要包括四种生活规律群体：(1)生活规律标准消费群体；(2)生活不规律、早餐不规律、校外就餐；(3)生活不规律、喜欢购物、校内消费、不爱吃早餐；(4)生活不规律、打水少、校外居住。

3)学习强度群体占比
用户可以查看所有年级中学生的学习强度群体占比情况，发现哪类是本校年级中的主流群体。用户进入学生图书门禁大数据平台后，选择下拉框中的某个要查找的年级，点击查询按钮后，系统会将该年级的学习强度群体占比值进行展示，主要包括四种群体：(1)学习强度强；(2)学习强度一般；(3)学习强度低；(4)学习强度较高。
### 系统运行效果图
省份消费地图

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095305_f726febf_1800784.png "省份消费地图.png")

省份消费排行top10

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095321_6eb4a500_1800784.png "省份消费排行.png")

个人消费频次统计图

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095345_1ab34f8b_1800784.png "个人消费频次.png")

个人类型消费统计图

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095357_2201cf23_1800784.png "个人消费统计.png")

图书借阅类型特点画像图

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095411_5df75af7_1800784.png "图书借阅画像.png")

学习强度占比图

![输入图片说明](https://images.gitee.com/uploads/images/2019/0528/095423_a35fada9_1800784.png "学习强度.png")


