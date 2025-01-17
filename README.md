## 游戏简介

欢迎来到贪吃蛇游戏！

该项目由C++和Qt制作，遵循GPL3.0协议。

已编译的游戏文件在./Game目录下


游戏说明：

本游戏分为经典模式和闯关模式，两者模式均有成就排行榜。

经典模式与传统的贪吃蛇玩法类似，不同的在该模式下用户可以自定义蛇的速度，食物数量，地图大小，蛇撞到身体或墙的状况。

闯关模式，则是在基本的贪吃蛇玩法下增加了障碍物和升级功能。玩家可以自定义地图，地图中可以自定义蛇的出生点，还提供了多种障碍物和升级机制。但蛇的速度，食物数量，地图大小，蛇撞到身体或墙的状况不可修改。

详细游戏说明请看其他页面的帮助。


游戏操作：
W，S，A，D分别控制蛇向上，下，左，右走。也可用方向键控制，此时蛇的行走方向与方向键方向相同。

## 自由模式

自由模式：

在自由模式下，游戏地图中毫无障碍物，还可修改游戏的多种属性。需要注意的是，为了保证公平公正，若玩家把随机食物的数量设置成超过1，或者游戏模式中，蛇撞到边界或自身不会死亡时，玩家的分数将不会进入排行榜。

游戏操作说明请看“游戏简介”。在游戏过程中，玩家可以随时暂停，不过不能保存游戏进度。玩家在中途退出游戏不会获得游戏分数，只有蛇死亡或玩家点击重新开始并确认，才能获得游戏得分。

当蛇吃掉一个食物时，玩家得1分。玩家的排行榜依次得分，时间，操作步骤进行排序。得分越高越好，时间和操作步骤越少越好。

（注：点击“重新开始”按钮时游戏会自动暂停，弹出选择框后让用户再次确定是否重新开始，不会立即重新开始）

## 闯关模式

闯关模式：

游戏规则：

在闯关模式下，玩家可以自由选择不同地图。地图中最多出现8种不同的障碍物。对应从0~8八个等级，约高等级的障碍物越坚硬，而蛇的等级也可以分为0~8八个等级，第i个等级的蛇可以破坏掉小于等于第i个等级的障碍物。

若蛇碰到比自身等级更高的障碍物，则会死亡。同时，蛇头撞到自己的身体或地图边界，也会死亡。

当蛇吃掉一个食物时，玩家得1分，蛇吃掉一个特殊食物，玩家得3分，并提升一级。玩家的排行榜依次得分，时间，操作步骤进行排序。得分越高越好，时间和操作步骤越少越好。必须要在已经定型的地图上玩家才能获取游戏分数，否则不能。关于“地图定型”的概念详见帮助文档的“地图设计”。

蛇的模样会因为蛇的等级而改变，下表展示了蛇的等级，蛇的模样和能破坏的最硬的障碍物的对照表。

## 地图编辑

地图的增删操作可以在闯关模式中的选择地图关卡的界面进行。界面中右上角的列表显示的是目前可以游玩的地图。地图上的字母H，B，T分别表示蛇头，蛇身，蛇尾的出生点，而且蛇的长度为3.

列表下方有个“地图定型”字样的选择框，表示地图是否定型。关于地图定型的概念，详见帮助文档的“地图设计”。

选中界面右上角列表中的地图后，玩家可以点击“开始”，“编辑”按钮进入地图开始游戏或者进入地图进行编辑。点击“删除”按钮可以删除地图。若要新建地图，则直接点击“新建”即可，无需选中某一块地图，即可新建一个空白地图进行编辑。

值得注意的是，地图定型状态显示打钩的地图为已经定型的地图，即是无法修改的地图。选中地图进行编辑时，若该地图已定型，则无法在原地图上修改，只能以定型的地图为基础，新建一个地图。详细操作见帮助文档的“地图设计”。

## 地图设计

用户可以在地图中设置蛇的出生点，游戏一开始时蛇头的方向，和绘制多种障碍物的地图，和设置特殊食物出现的位置。


基本操作方式：

在设置方块的组合框中选择玩家要使用的方块，在地图编辑页面左边的大网格中，鼠标左键即可在鼠标位置的方格中放置，鼠标右键则会清除在这格子中的所有方块，但蛇的头，身，尾不能清除，只能改变位置。蛇的出生点设置方法略有不同，请见下文。


设置蛇的出生点：

除了蛇的出生点外，特殊食物和障碍物等方块的放置方式不限。蛇必须有出生点，而且出生点唯一。地图编辑器上分别用head，body，tail的大写首字母H，B，T表示蛇头，蛇身，蛇尾。分别对应长度为3的蛇的三个部分

三者的位置都能随意放置，并通过“蛇的方向”组合框来决定游戏开始时蛇头的前进方向。值得注意的是，为了让游戏具有灵活性，蛇头，蛇身，和蛇尾的出生点不必连在一起，而游戏开始后蛇的3节身体会自动连接。在一些特殊的地图可以灵活设置。


地图定型：

为了保证游戏的公平性，游戏加入了地图定型功能。顾名思义，已经定型的地图将无法进行修改，保证了玩家分数的真实性。勾选地图中的地图定型选项，点击“保存”后，再次确认，地图即无法继续修改。至于如何在已经定型的地图上设计地图，详见下文“地图保存”。


地图保存：
点击“保存”按钮即可保存地图。其中“文件名”里填的是保存地图时地图的名称。要保存的地图的名称不能与已经定型的地图重名！若要在已经定型的地图的基础上修改，需要保存为新的地图，更改文件名即可。
