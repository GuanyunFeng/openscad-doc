# openscad中文教程
　　OpenSCAD 是一款可靠的 3D 建模器，能够使用其脚本语言创建参数模型。与大多数用于创建3D模型的免费软件不同，OpenSCAD侧重于CAD方面，而不是3D建模的艺术方面。因此，OpenSCAD主要用于创建机器零件的 3D 模型时要查找的应用程序，但不适用于创建计算机动画电影。本教程部分案例来自于官网，但重新进行了整理。
## 1.创建基础图形
基础的3D图形包含：</br>
　　1.cube 长方体 </br>
　　2.cylinder 圆柱体</br>
　　3.sphere 圆球</br>
　　4.polyhedron 多边体</br></br>
当绘制图形的时候，其生成的位置会基于三维坐标系中的一个坐标。默认的坐标是(0,0,0),这一坐标也可以使用translate进行修改。
### 长方体
长方体的函数为```cube(size=1,center=false)```,包含以下参数:</br>
　　**center**:默认为false,其中(0,0,0)是长方体坐标做小的顶点。若指定center为true,(0,0,0)是长方体的中心。</br>
　　**size**: 默认值为1。size可以指定为单个数值，或数值三元组如[1,2,3]。若指定size为单个数值，则生成正方体，size是其楞长。若指定size为三元组[x,y,z],则x、y、z分别是长方体x轴、y轴、z轴上的棱长。</br>
示例一:```cube(size = 10)```</br>
![cube1](https://github.com/GuanyunFeng/openscad-doc/blob/main/imgs/cube1.png)</br>
示例二:```cube(size = 10, center = true)```</br>
![cube2](https://github.com/GuanyunFeng/openscad-doc/blob/main/imgs/cube2.png)</br>
示例三:```cube(size = [5,10,15])```</br>
![cube3](https://github.com/GuanyunFeng/openscad-doc/blob/main/imgs/cube3.png)</br>

### 圆柱体
圆柱体的函数为```cube(h = 1, r = 1, r1 = 1, r2 = 1, d = 2, d1 = 2, d2 = 2, center=false)```,不仅可以绘制圆柱体，还可以绘制圆台和圆锥。其包含以下参数:</br>
　　**center**:默认为false,其中(0,0,0)是圆柱底面圆心坐标。若指定center为true,(0,0,0)是圆柱体的中心。</br>
　　**h**:默认值为1。h是圆柱体的高。</br>
　　**r**: 默认值为1。r是圆柱上下圆形的半径。若指定了r,则参数r1,r2,d,d1,d2失效。</br>
　　**r1**: 默认值为1。r1是底面圆形半径。若指定了r1,则参数r,d,d1,d2失效，圆柱上下底面圆形的大小由r1和r2决定。</br>
　　**r2**: 默认值为1。r2是顶面圆形半径。若指定了r2,则参数r,d,d1,d2失效，圆柱上下底面圆形的大小由r1和r2决定。</br>
　　**d**: 默认值为2。d是圆柱上下圆形的直径。若指定了d,则参数r,r1,r2,d1,d2失效。</br>
　　**d1**: 默认值为2。d1是底面圆形直径。若指定了d1,则参数r,r1,r2,d失效，圆柱上下底面圆形的大小由d1和d2决定。</br>
　　**d2**: 默认值为2。r2是顶面圆形直径。若指定了d2,则参数r,r1,r2,d失效，圆柱上下底面圆形的大小由d1和d2决定。</br>

示例一:```cube(size = 10)```</br>
![cube1](https://github.com/GuanyunFeng/openscad-doc/blob/main/imgs/cube1.png)</br>
示例二:```cube(size = 10, center = true)```</br>
![cube2](https://github.com/GuanyunFeng/openscad-doc/blob/main/imgs/cube2.png)</br>
示例三:```cube(size = [5,10,15])```</br>
![cube3](https://github.com/GuanyunFeng/openscad-doc/blob/main/imgs/cube3.png)</br>
