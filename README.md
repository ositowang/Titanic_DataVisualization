# Titanic_DataVisualization
Data Visulization with D3 and dimple.js
# Titanic_DataVisualization
Data Visualization with d3.js and dimple.js
1. 项目简介
本项目使用了kaggle提供的Titanic乘客的数据集。数据集包括了乘客的生还情况，乘客之间的关系，和他们所在船舱位置的基本情况等等。
本可视化旨在通过交互式的可视化探究乘客生还情况与他们的社会和经济地位情况之间的关系。
在本项目中使用d3.js和dimple.js进行交互式可视化，使用了python进行数据预处理。
2. 可视化设计概述
本项目使用了堆叠条形图对数据进行了可视化， 主要统计了不同年龄段的乘客，在不同舱位，不同登船地点，不同性别三个层面上的乘客成活数量情况。
本可视化旨在帮助读者探索可能导致乘客成活的不同因素，并对更深层次的数据挖掘提供了初步的思路。
3. 可视化设计
本数据取自kaggle的统计数据集，由于本数据基本是非常干净数据集。我在可视化之前，仅对数据集进行了小范围的修改，提高了数据可读性。
此外我还根据普遍年龄划分的习惯，对年龄进行了重新分组，0-16岁为儿童14-40位青年，40-60为中年，60以上为老年。此外，由于数据中年龄
包含缺失值，由于在可视化中我们将要添加年龄作为分类变量，所以我将数据集中年龄为空值的数据行进行了移除处理。此外我还移除了登船地点
为空值的数据行。具体的数据清理过程可以参见如下代码：
https://github.com/ositowang/Titanic_DataVisualization/blob/master/Data_Preprocessing.ipynb
4. 数据可视化工具
在本项目中，我主要使用了dimple.js进行了数据可视化，以及利用d3.js进行了更新和数据注解工作。在本项目中，我一共进行了2次迭代设计过程，
从静态的图表演变为简单的可交互式图表，并为故事背景添加了介绍和链接以便读者了解真个故事的概况。
5. 设计迭代过程
5.1 初步设计
在最初的可视化设计中，我根据性别，年龄和成活数量，对数据进行了可视化，我运用堆叠条形图对数据进行了展示，用颜色进行了性别的分类，横坐标
为分类变量，纵坐标为度量。在颜色上，我选择了颜色区别较为明显的三种颜色，并避免了非常刺眼的大红或者大黄色造成读者的视觉疲劳。此外，我还为
可视化添加了标题并将其居中显示。
具体的代码可以参见index_first.html,或参见以下截图。
！[image](https://github.com/ositowang/Titanic_DataVisualization/blob/master/Initial_Design.PNG)

5.2 征求读者意见
在完成了初步设计后，我将数据可视化展示给了三位同学，获得了如下反馈：

反馈1
整体可视化比较清晰，有清晰的横纵坐标轴标注，读者可以清楚的解读横纵坐标的意义。美中不足的是图例的尺寸较小，相对于巨大的条形来说显得
不是很明显。
反馈2
整体可视化清晰的传达了数据的构成和数量，美中不足的是可视化只是静态的图表，如果可以添加一下互动元素则更好。
反馈3
整体的可视化非常清晰，但是存在着语言统一的问题，如果将图中的语言进行统一，会显得更加专业一些。此外，如果能给可视化添加一些背景知识，
有助于读者理解你的可视化。
根据以上意见反馈，我进行了两次迭代设计。

5.3 第二次设计
在第二次设计中，我为图表添加了简单的交互功能，提供了按舱位，按性别和按登船地三种交互选项，以便读者可以根据自己的需要对数据集进行探索。
此外我简单的调整了条形图的宽度，使其看起来更加美观并适当增加了图例的大小。
！[image](https://github.com/ositowang/Titanic_DataVisualization/blob/master/Second_Design.PNG)

5.4 第三次设计
在第三次设计中，我统一了交互选项的语言和横纵坐标轴的标注。此外，我还添加了标题和背景说明文件，在背景说明文件中添加了超链接视频，以便读者
能够更好的了解这个背景故事的概况。此外，我还调整了三个交互选项的位置，为其提供了统一的样式和位置，提高了整体的美观性。并且根据交互选项，我
在图表的侧面添加了图表说明文件为读者阐释一些基本的数据情况。不同的交互选项，还为分类变量提供了不同的颜色类型。最后，利用框架调整了整体的
网页布局，使其看起来更加读者友好。
！[image](https://github.com/ositowang/Titanic_DataVisualization/blob/master/Final_Design.PNG)
