MVC为Model-View-Controller，为模型(保存数据)-视图(用户界面)-控制器(处理业务逻辑)
1.view传送指令到controller
2.Controller完成业务逻辑后，要求model改变状态
3.model将新的数据发送到view，用户得到反馈
MVP为Mode-View-Presenter
1.各部分的通信都是双向的
2.view和model不发生联系，都靠presenter传递
3.view不部署任何业务逻辑，所有业务逻辑都部署在Presenter
MVVM为Mode-View-ViewModel
基本和MVP一致，唯一的区别MVVM使用数据双向绑定
View的变化会自动更新到ViewModel,ViewModel的变化也会自动同步到View上显示
这种同步是因为ViewModel中的属性实现了Observer