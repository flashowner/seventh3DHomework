# 彩虹光环和宇宙大爆炸效果
彩虹光环的实现：<br>
彩虹光环由七个光环组成，分别是红橙黄绿青蓝紫，其中红，黄，青，紫光环是按照顺时针旋转的，<br>
其余的光环是按照逆时针旋转的,效果图如下所示：<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B7.PNG)<br>
因为七个彩虹光环的动作都是相似的，只是旋转方向和颜色不同，因此只要明白其中一个光环是如<br>
何实现的，剩下的就可以仿照完成的光环来实现。首先先创建一个空对象ParticleRing来容纳所有<br>
的光环，在这个空对象里再创建一个空对象ring_inner表示红色光环，选择ring_inner添加组件-><br>
Effects->Particle System：<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B71.PNG)<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B72.PNG)<br>
定义结构CirclePosition，用来记录每个粒子的当前半径、角度和时间，其中时间是做游离运动需要的<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B73.PNG)<br>
定义需要使用的变量：<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B74.PNG)<br>
初始化设置：<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B75.PNG)<br>
随机设置粒子出现时的位置，但是位置要在最大半径和最小半径之间：<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B76.PNG)<br>
最后是设置粒子的旋转：<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B77.PNG)<br>
这样彩虹光环的红色光环就完成了，其余的光环只需要修改粒子颜色和最大最小半径就可以实现了.<br>
宇宙爆炸的实现效果如下：<br>
![](https://github.com/flashowner/seventh3DHomework/blob/master/%E5%9B%BE%E7%89%87/%E6%8D%95%E8%8E%B78.PNG)<br>
先是聚拢粒子，然后是喷射粒子，最后只剩下稀疏的粒子在进行移动，宇宙爆炸效果的实现越光环<br>
的实现基本一样，只是将粒子颜色改成白色，以及将游离范围设置成1.<br>
代码位置：https://github.com/flashowner/seventh3DHomework/tree/master/Scripts
