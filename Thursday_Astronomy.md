# 科学与工程中的线性与非线性：人工智能与弯曲时空：李惕碚T.P.Li

[TOC]

	Tips:
	直接解调方法：direct demodulation method
	
## 线性与非线性
	21世纪是非线性应用的世纪
- 上世纪科学主要是建立在线性数学上
- 非线性数学非常困难

## 经历
- 1963年工物毕业
- 毕业分配到云南东川宇宙线观测站，建造云雾室
	- 云雾室温度要控制恒定
	- PID控制器（比例-积分-微分）
			比例微分系数大：振荡趋近
			比例积分系数大：平稳，不穿过，无限趋近
			加入开关拔掉干预，则可以很良好地解决问题：将开关拔掉是一个非线性控制
			现今的人工神经网络便是非线性

## 人工智能与慧眼卫星
### X射线天文
- 1962年 贾科尼Giacconi 第一次发现天空中X射线源
- 小田发明扫描（线性）调制方法，最小二乘拟合数据，获得位置信息
		最小二乘法是解决逆问题的
		人工智能是逆问题的一种
- Uhuru第一颗天文X射线卫星
- 10-250keV能区空白，需要硬X射线巡天，小田的方法在高能上已经不可用
- 编码孔径成像：成像复杂，需要解调
$$
Pf=d
$$
$$
c=P^Td
$$

- 硬X射线探测器：Integral,Swift

- [x]李惕碚、吴枚：***直接解调方法***
- 如果直接同线性方法解，会出现负解、非物理解
- 在非线性约束下迭代解方程,而不是用最小二乘法直接乘逆
- 非线性约束：当$ f_{i}<0 $时，令$ f_{i}=0 $

- 1993年，我国科学家提出建设硬X射线天文望远镜HXMT
- 如何如此延期？
	- [x] 对直接解调方法不信任，周光召质疑稳定性和收敛性问题:
			- 思考，发现与神经网络相关
			- Hopfield网络，已经由数学证明收敛
	- [x] 即使国际上已经认可，但国内学术界的抨击，决定仪器寒酸，不相信能取得很好的结果，认为paper没有引用率
	- [x] 2006年后经费问题
			2009年Science专文评述HXMT项目现状:中国的HXMT是不是永远只能停在地面？
- 2011.3工程立项
- 2017年.6.15酒泉发射

|Satellite|Theory Start|Application|
|:---:|:---:|:---:|
|HXMT|1992|2017|
|Uhuru|1965|1970|

	1993-2006坐以论道13年，质疑的人没有一个动手去算

~~~mermaid
graph LR
	B(1992)-->C((2006))
	C-->D[2011]
	D-->E{2017}
~~~

## 弯曲时空与引力波
- 引力与加速坐标系的等效只在无穷小区域内成立
- 爱因斯坦方程：
$$
G_{\mu\nu}(g_{\mu\nu},\dot{g}_{\mu\nu},\ddot{g}_{\mu\nu})=8\pi GT_{\mu\nu}
$$
逐步迭代的方法去解

- 中国思考：周培源反对爱因斯坦弯曲时空：认为引力的物理实在性，弯曲时空是数学的；认为运动的时空依然是平直的；彭恒武赞同；

- 弯曲时空不能产生引力波？爱因斯坦本身就发现从弯曲时空的观点导出的引力波可以不带能量，是表观波，取决于参考系
	- 引力辐射阻尼问题，胡宁计算，发现阻尼为负，发现引力波辐射增加了系统的能量
	> 一个描述局域系统的理论需要无穷远处的物理条件，显示这个理论框架存在根本的问题
	- 尾状物问题，应该在弯曲时空中来回反射，有尾状物
	- 下落和固定的物体，谁会辐射？
	- 平直时空就不能产生引力波吗？
		- 引力波和光都在光锥上传播，会与光发生影响，因此用激光干涉才能探测出引力波，而用物质不行；引力波并不是时空涟漪，而是一种物理波
		- LIGO的臂并不是实物变形，而只是引起了激光的影响
				引力和电磁类似？运动质量产生引力的另一个力？矢量势导致引力波的产生
		- 宇宙提供了一个绝对的惯性参考系
			- WMAP的图数据纠正，宇宙组成比例调整
			- Axis of evil and 25.6ms
			- 两个时钟差距25.6ms
			- 没有扣除多普勒效应，造成宇宙背景有极性
			- 扣除后，几乎绝对均匀，0.7%的涨落
			- Planck卫星证实
			- ***宇宙存在绝对的惯性系***

## Questions
- 要辐射电磁波需要加速度，那么要辐射引力波也要加速（即产生“引力”）
- 加速度的相对性与能量损失问题？
- 电与磁，引力的另一个伙伴呢？？磁性引力？
- 现在利用直接解调方法的卫星除了HXMT还有其他吗？国内外