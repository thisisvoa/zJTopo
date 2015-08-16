# zJTopo
开源拓扑图工具类jTopo的扩展

说明
-----------------------------------
该项目依赖于开源拓扑图工具类jTopo,详情:[JTopo](http://www.jtopo.com/)<br />
联系本人:799378666@qq.com


###扩展api简介
	///获取该场景下所有元素<br>
	JTopo.Scene.prototype.zGetAllEle()<br>
	///将该场景转换为json形式<br>
	JTopo.Scene.prototype.zToJson()<br>
	///将json数据解析到该场景中,加载ems里面的对象以及偏移量(translateX,translateY)
	JTopo.Scene.prototype.zLoadJson(json)
	///通过params的idA与idZ来连线,或通过nodeA与nodeZ来连线(优先)
	JTopo.Scene.prototype.zAddLink 
	///通过params来创建Node节点
	JTopo.Scene.prototype.zAddNode<br>
	///设置开始节点,会开启画线模式,会从该节点处引出一条线
	JTopo.Scene.prototype.zSetStartLinkNode
	///开始连线模式
	JTopo.Scene.prototype.zStartLinkModel
	///关闭连线模式,会清空一些临时连线对象
	JTopo.Scene.prototype.zCloseLinkModel
	///放大(动画版),与原生的放大不一样!,放大1.1表示在原来的基础上乘以1.1
	JTopo.Scene.prototype.zZoomOut
	///缩小(动画版),与原生的缩小不一样!,缩小1.1表示在原来的基础上除以1.1
	JTopo.Scene.prototype.zZoomIn
	///缩放到指定比例(动画版)
	JTopo.Scene.prototype.zZoom
	//将某个元素获得焦点并居中(动画版)
	//参数params为json对象,其中speed为动画持续时间, jquery中的那种动画,x,y为将该元素移动到某个点,默认为画布宽高的一半
	JTopo.Scene.prototype.zFocusEle
	///自适应,将使最左的元素贴近场景左边,使最上的元素靠近场景的上边,重置缩放比例为1:1(动画版)
	///参数:left距离左边的距离,top,距离上边的距离
	JTopo.Scene.prototype.zAdaptive
	///为舞台增加一个场景,只有调用该方法增加的场景才能有连线模式,才会能够使用其他功能
	JTopo.Stage.prototype.zCreateScene
	//回退场景,需要通过zCreateScene创建的场景才能回退
	JTopo.Stage.prototype.zBack
	///画布全屏
	JTopo.Stage.prototype.zFullScreen