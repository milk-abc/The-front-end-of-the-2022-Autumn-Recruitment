合批渲染

mergeGeometries

它是利用颜色的6位16进制表示，以颜色作为ID，在后台渲染出纹理后，根据鼠标坐标下的纹理颜色，进行ID的查询进行拾取操作。

就是将纹理材质用id存储，取纹理像素就是取对应的id

将拾取的材质放入缓冲区内，渲染拾取的场景，创建buffer用来读取拾取的纹理，读取出来的纹理像素就是空间数据的id，

遍历场景中的所有物体，给这些物体加上唯一的id，将id通过顶点着色器传给片元着色器作为纹理的输出，创建一个后台缓冲区，将场景用该纹理进行渲染，根据鼠标坐标下的纹理像素，可以读取出对应的id，从而取出对应的对象

缺点：

1.需要用空间换时间，还要弄一个拾取的场景，并渲染它

2.需要用一个数组存储场景对象的positions

存储消耗很大



视锥裁剪

矩阵变换
