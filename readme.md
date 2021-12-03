# 3DExample

## 参考链接

* [720云](https://720yun.com/)
* [720云教程](https://www.sveltejs.cn/)
* [720云教程汇总](https://bbs2.720yun.com/article?id=234)
* [Krpano](http://www.krpano360.com/)
* [krpano英文文档](https://krpano.com/home/)
* [不到30行代码实现一个酷炫H5全景](https://juejin.cn/post/6968263858309824526)
* [三种前端实现VR全景看房的方案！说不定哪天就用得上！](https://juejin.cn/post/6973865268426571784)
* [three.js github](https://github.com/mrdoob/three.js/tree/master)
* [threejs官方立方体全景示例](https://github.com/mrdoob/three.js/blob/master/examples/webgl_panorama_cube.html)
* [threejs官方球体全景示例](https://github.com/mrdoob/three.js/blob/master/examples/webgl_panorama_equirectangular.html)
* [css3d-engine](https://github.com/shrekshrek/css3d-engine)
* [2天赚了4个W，手把手教你用Threejs搭建一个Web3D汽车展厅！](https://juejin.cn/post/6981249521258856456)
* [threejs editor](https://threejs.org/editor/)
* [three.js 相机的详细介绍（04）](https://blog.csdn.net/weixin_48931875/article/details/113781252)
* [96 Three.js 使用cubeCamera相机创建反光效果](https://blog.csdn.net/qq_30100043/article/details/80187684)
* [Three.js - 光源使用详解1（环境光 AmbientLight、点光源 PointLint）](https://www.hangge.com/blog/cache/detail_1810.html)
* [three.js 光的介绍（05）](https://blog.csdn.net/weixin_48931875/article/details/113858358)
* [three.js 点、线、坐标轴（02）](https://blog.csdn.net/weixin_48931875/article/details/113753930)
* [three.js 纹理（06）](https://blog.csdn.net/weixin_48931875/article/details/113887970)
* [three.js 着色器（08）](https://blog.csdn.net/weixin_48931875/article/details/114585456)
* [three.js 运动吧物体（03）](https://blog.csdn.net/weixin_48931875/article/details/113775632)
* [stats](https://github.com/mrdoob/stats.js)
* [ThreeJS中的点击与交互——Raycaster的用法](https://www.cnblogs.com/lst619247/p/9071233.html)
* [Three.js中文教程](https://techbrood.com/threejs/docs/)

## 目录

* [3D方案](#3D方案)
* [threejs](#threejs)
    * [场景（scene）](#场景（scene）)
        * [容器](#容器)
        * [坐标系](#坐标系)
    * [摄像机（camera）](#摄像机（camera）)
        * [透视相机PerspectiveCamera](#透视相机PerspectiveCamera)
        * [正交相机OrthographicCamera](#正交相机OrthographicCamera)
        * [立方体相机CubeCamera](#立方体相机CubeCamera)
        * [相机的位置、方向、看向](#相机的位置、方向、看向)
        * [在球坐标中的相机转动](#在球坐标中的相机转动)
    * [渲染器（renderer）](#渲染器（renderer）)
    * [着色器（shader）](#着色器（shader）)
    * [几何体（geometry）](#几何体（geometry）)
        * [点](#点)
        * [线](#线)
        * [PlaneGeometry（平面几何体）](#PlaneGeometry（平面几何体）)
        * [CircleGeometry（圆形几何体）](#CircleGeometry（圆形几何体）)
        * [RingGeometry（环形几何体）](#RingGeometry（环形几何体）)
        * [ShapeGeometry（形状几何体）](#ShapeGeometry（形状几何体）)
        * [BoxGeometry（立方几何体）](#BoxGeometry（立方几何体）)
        * [SphereGeometry（球几何体）](#SphereGeometry（球几何体）)
        * [CylinderGeometry（圆柱几何体）](#CylinderGeometry（圆柱几何体）)
        * [ConeGeometry（圆锥几何体）](#ConeGeometry（圆锥几何体）)
        * [TorusGeometry（圆环几何体）](#TorusGeometry（圆环几何体）)
        * [TetrahedronGeometry（四面几何体，三棱锥）](#TetrahedronGeometry（四面几何体，三棱锥）)
        * [OctahedronGeometry（八面几何体，双面三棱锥）](#OctahedronGeometry（八面几何体，双面三棱锥）)
        * [DodecahedronGeometry（十二面几何体，正五边形十二面体）](#DodecahedronGeometry（十二面几何体，正五边形十二面体）)
        * [IcosahedronGeometry（二十面几何体，正三边形十二面体）](#IcosahedronGeometry（二十面几何体，正三边形十二面体）)
        * [PolyhedronGeometry（多面几何体）](#PolyhedronGeometry（多面几何体）)
        * [TorusKnotGeometry（圆环扭结几何体）](#TorusKnotGeometry（圆环扭结几何体）)
        * [TubeGeometry（管道几何体）](#TubeGeometry（管道几何体）)
        * [ExtrudeGeometry（挤压几何体）](#ExtrudeGeometry（挤压几何体）)
        * [LatheGeometry（车削几何体，带洞灯罩）](#LatheGeometry（车削几何体，带洞灯罩）)
        * [Geometry（自定义几何体）](#Geometry（自定义几何体）)
        * [ParametricGeometry（参数化几何体）](#ParametricGeometry（参数化几何体）)
        * [TextGeometry（文本几何体）](#TextGeometry（文本几何体）)
    * [灯光（light）](#灯光（light）)
        * [AmbientLight（环境光，没有方向全局打亮，不会产生明暗）](#AmbientLight（环境光，没有方向全局打亮，不会产生明暗）)
        * [DirectionLight（平行光，无衰减，参考日光来理解）](#DirectionLight（平行光，无衰减，参考日光来理解）)
        * [PointLight（点光源，参考灯泡来理解）](#PointLight（点光源，参考灯泡来理解）)
        * [SpotLight（聚光灯，有衰减，参考舞台聚光灯）](#SpotLight（聚光灯，有衰减，参考舞台聚光灯）)
    * [纹理（texture）](#纹理（texture）)
    * [贴图（texture）](#贴图（texture）)
    * [材质（material）](#材质（material）)
    * [3d模型的文件格式](#3d模型的文件格式)
    * [信息点](#信息点)
    * [性能监视器Stats](#性能监视器Stats)
    * [平台](#平台)
    * [优化](#优化)
    * [样例](#样例)
        * [球形3D漫游](#球形3D漫游)
        * [立方体3D漫游](#立方体3D漫游)
* [更加轻量的3D引擎(css3d)](#更加轻量的3D引擎(css3d))

---

## 3D方案

* 技术调研

    以下网站实现全景图VR漫游，均基于Krpano：

    需给钱：pano2vr、playcanvas、得图云、airpano、720云、动景网、全景客、ivrpano、全景旅行者、光鱼全景、全景云、720think、三维家、视网、网展

    krpano核心是js/flash/html5/xml，支持webGL下的webVR

    其它实现方法：CSS3 3D，ThreeJS

* 720制作方法

    1. 根据教程导图
    2. 在线制作全景图VR漫游
    3. 开通vip下载离线包，部署到自己的网站
    4. iframe嵌套，添加其它功能

* WebGL3D引擎(three.js,babylon.js,playcanvas)

## threejs

### 场景（scene）

#### 容器

容纳着除渲染器以外的三维世界里的一切。

#### 坐标系

场景的元素采用右手笛卡尔坐标系，x轴正方向向右，y轴正方向向上，z轴由屏幕从里向外

* 世界坐标

一个应用程序可能包含成百上千个单独的对象，我们必须把他们放到一个公共的场景里，这个公共的场景就叫做世界坐标。

* 相机默认在世界坐标的原点
* 3D屏幕中的所有物体都可以在该坐标系系统下移动和旋转
* 对于屏幕上所有的物体来说，这个坐标系是相同的，并且它不会改变
* 用户默认的观察视角是沿着Z轴的负半轴方向
* 世界坐标系是以屏幕中心为原点(0, 0, 0)，且是始终不变的
* 你的右边是x正轴，上面是y正轴，屏幕指向你的为z正轴
* 窗口范围按此单位恰好是(-1,-1)到(1,1)，即屏幕左下角坐标为（-1，-1），右上角坐标为（1,1）

* 本地坐标

物体的本身的坐标，即物体中心点。

* 屏幕坐标系

webGL的重要功能之一就是将三维的世界坐标经过变换、投影等计算，最终算出它在显示设备上对应的位置，这个位置就称为设备坐标。在屏幕、打印机等设备上的坐标是二维坐标。

* 视点坐标系

是以视点（照相机）为原点，以视线的方向为Z+轴正方向的坐标系中的方向。webGL会将世界坐标先变换到视点坐标，然后进行裁剪，只有在视线范围(视见体)之内的场景才会进入下一阶段的计算。

* AxesHelper三维坐标系

    * 可以在场景中添加辅助坐标系帮助开发
    * 可以使物体绕着本地坐标系旋转，而不绕世界坐标系旋转
    * 用于简单模拟3个坐标轴的对象（红色代表x轴，绿色代表y轴，蓝色代表z轴）

    ```js
    var axeshelper = new THREE.AxesHelper(5);
    axesHelper.rotation.y -=0.01; //围绕坐标轴旋转
    scene.add(axeshelper)
    ```

* 网格辅助

    ```js
    let gridHelper = new THREE.GridHelper(10, 1, "f0f0f0", "ffffff");//网格大小、步长、中线颜色、网格颜色
    gridHelper.position.x = 10;
    gridHelper.position.y = 2;
    gridHelper.position.z = 10;
    scene.add(gridHelper);
    ```

### 摄像机（camera）

在一个空间里可以看向任意方向，可以通过参数调节可视角度和可视距离。

#### 透视相机PerspectiveCamera

符合物理世界近大远小真实情况
```js
PerspectiveCamera( fov : Number, aspect : Number, near : Number, far : Number )
//构造函数参数
//fov：视场角，眼睛睁开的角度，即视角大小。如果设置为0，相当于闭上了眼睛，故什么也看不见；如果为180，看以认为视角很广阔。但是在180度时，物体会很小，因为物体在整个可视区域中的比例变小了。
//aspect：视场宽高比，窗口的纵横比，即宽度除以高度。这个值越大，表示宽度越大，那么看的就越宽；否则看的就越窄。（一般用 画布宽/画布 高即可）
//near：能看多近，眼睛距离近处的距离。不可以设置为负值。
//far：能看多远
//这几个参数决定了哪些scene里的三维顶点会被渲染/绘制出来
```

#### 正交相机OrthographicCamera

远近大小是一样的
```js
OrthographicCamera(left,right,top,bottom,near,far)
//left：左平面距离相机中心点的垂直距离。
//right：右平面距离相机中心点的垂直距离。
//top：顶平面距离相机中心点的垂直距离。
//bottom：底平面距离相机中心点的垂直距离。
//near：近平面距离相机中心点的垂直距离。
//far：远平面距离相机中心点的垂直距离。
var camera = new THREE.OrthographicCamera(width/-2,width/2,height/2,height/-2,1,1000);
//将浏览器窗口的高度和宽度作为了视景体的高度和宽度，相机正好在窗口的中心点上
```

#### 立方体相机CubeCamera

为场景中的所要渲染的物体创建快照,创建反光效果
```js
//CubeCamera（near：Number，far：Number，cubeResolution：Number）
//近 - 近裁剪距离。
//远 - 裁剪距离
//cubeResolution - 设置立方体边缘的长度。

//可以通过renderTarget对象获取生成的立方体纹理。
//创建一个获取环境贴图的cubeCamera
cubeCamera = new THREE.CubeCamera(0.1, 1000, 256);
scene.add(cubeCamera);
```

#### 相机的位置、方向、看向

```js
var camera = new THREE.PerspectiveCamera(45,width/height,1,1000);
//表示相机的位置
camera.position.x = 0;
camera.position.y = 0;
camera.position.z = 600;
//表示相机以哪个方向为上方，相当于真实相机的快门朝向
camera.up.x = 0;
camera.up.y = 1;
camera.up.z = 0;
//相机看向的坐标，即相机的中心镜头对准哪里
camera,lookAt({
    x:0,
    y:0,
    z:0
});
```

#### 在球坐标中的相机转动

```txt
推导相机朝向方向
相机朝向A(x0,y0,z0),圆点O,AO垂直夹角(纬度lat)y,水平夹角(经度lon)x
x0=r在x轴上投影=r在xz平面投影在x轴上投影=rsin(y)cos(x)
y0=r在y轴上投影=rsin(y)
z0=r在z轴上投影=r在xz平面投影在z轴上投影=rsin(y)sin(x)
```

```js
lat = Math.max(- 85, Math.min(85, lat));//纬度限制在[-85°,85°]
phi = THREE.Math.degToRad(90 - lat);//与y轴夹角，y轴正方向为90°
theta = THREE.Math.degToRad(lon);//与x轴夹角
//相机旋转
camera.target.x = scene_radius * Math.sin(phi) * Math.cos(theta);//r在x轴上投影=r在xz平面投影在x轴上投影=rsin(y)cos(x)
camera.target.y = scene_radius * Math.cos(phi);//r在y轴上投影=rsin(y)
camera.target.z = scene_radius * Math.sin(phi) * Math.sin(theta);//r在z轴上投影=r在xz平面投影在z轴上投影=rsin(y)sin(x)
camera.lookAt(camera.target);
```

### 渲染器（renderer）

将camera在scene里看到的内容渲染/绘制到画布上

* 物体运动的两种方法

    1. 让相机在坐标系里面移动，物体不动。
    2. 物体在坐标系里面移动，摄像机不动。

* 样例

    ```js
    function animate(){
        render();//to do
        requestAnimationFrame(animate);
    }
    ```

### 着色器（shader）

每一个图元都会先执行顶点着色器，然后再执行片元着色器。

shader程序就是在显卡中运行的，针对每一个顶点或者片元（像素），显卡将运行一次shader程序。每个顶点或者片元的shader程序在显卡中都是并行运行的，所以速度极快。

* 分类

    * 顶点着色器 ：就是对顶点进行操作。例如改变顶点的位置和顶点的大小。
    * 片元着色器 ：通俗讲就是用来定义屏幕中显示的各个点的颜色。

* 样例

    ```js
    var gl = renderer.context;

    var glVertexShader = new THREE.WebGLShader( gl, gl.VERTEX_SHADER, vertexSourceCode );
    var glFragmentShader = new THREE.WebGLShader( gl, gl.FRAGMENT_SHADER, fragmentSourceCode );

    var program = gl.createProgram();

    gl.attachShader( program, glVertexShader );
    gl.attachShader( program, glFragmentShader );

    gl.linkProgram( program );
    ```

### 几何体（geometry）

3D世界里的所有物体都是点组成面，面组成几何体

#### 点

```js
var point1 = new THREE.Vector3(2,3,4);
//第二种方法
var point1 = new THREE.Vector3();
point1.set(1,2,3);
```

#### 线

```js
var geometry = new THREE.BufferGeometry();  //声明一个几何体
var material = new THREE.LineBasicMaterial({vertexColors:true});  //定义线条的材质
//定义两种颜色，分别表示线条两个端点的颜色
var color1 = new THREE.Color(0x444444),color2 = new THREE.Color(0xFF0000);

//线的材质可以由两点的颜色决定
//定义两个顶点的位置，并放在几何体重
var p1 = new THREE.Vector3(-100,0,100);
var p2 = new THREE.Vector3(100,0,-100);
geometry.vertices.push(p1,p2);
//geometry.vertices.push(p2);
geometry.colors.push(color1,color2); //为物体添加颜色

//定义一条线
var line = new THREE.Line(geometry,material,THREE.LineSegments);
scene.add(line);
```

#### PlaneGeometry（平面几何体）

```js
var camera,scene,renderer;
var mesh;
init();
animate();

function init(){
    renderer = new THREE.WebGLRenderer();
    renderer.setSize(window.innerWidth,window.innerHeight);
    document.body.appendChild(renderer.domElement);

    camera = new THREE.PerspectiveCamera(70,window.innerHeight/window.innerHeight,1,1000);
    camera.position.z = 400;
    scene = new THREE.Scene

    //x轴宽，y轴高，x轴分段数，y轴分段数
    var geometry = new THREE.PlaneGeometry(500,300,1,1);
    geometry.vertices[0].uv = new THREE.Vector2(0,0);
    geometry.vertices[1].uv = new THREE.Vector2(2,0);
    geometry.vertices[2].uv = new THREE.Vector2(2,2);
    geometry.vertices[3].uv = new THREE.Vector2(0,2);

    var texture = THREE.ImageUtils.loadTexture("index2.jpg",null,function(t){

    });

    var material = new THREE.MeshBasicMaterial({map:texture});
    var mesh = new THREE.Mesh(geometry,material);
    scene.add(mesh);

    window.addEventListener('resize',onwindowResize,false);
}

function animate(){
    requestAnimationFrame(animate);
    renderer.render(scene,camera);
}
```

#### CircleGeometry（圆形几何体）

```js
//radius — 圆的半径, 默认值 = 50.
//segments — 分割面数量 (三角形), 最低值 = 3, 默认值 = 8.
//thetaStart — 第一个分割面的开始角度, 默认值 = 0 (3点钟方向).
//thetaLength — 圆形扇形的圆心角通常称为θ。默认为2 * Pi，这形成了一个完整的圆
CircleGeometry(radius, segments, thetaStart, thetaLength)
```

#### RingGeometry（环形几何体）

```js
//innerRadius — 内半径默认值为0, 但是当值设为0的时候并不能正常工作.
//outerRadius — 外半径默认值为50.
//thetaSegments — 分割面数量. 更高的值意味着更加的圆滑. 最小值为3. 默认值为8.
//phiSegments — 最小值为1. 默认值为8.
//thetaStart — 第一个分割面的开始角度. 默认值为0.
//thetaLength — 圆形扇形的圆心角通常称为θ. 默认值为Math.PI * 2.
RingGeometry(innerRadius, outerRadius, thetaSegments, phiSegments, thetaStart, thetaLength)
```

#### ShapeGeometry（形状几何体）

```js
var rectLength = 120, rectWidth = 40;

var rectShape = new THREE.Shape();
rectShape.moveTo( 0,0 );
rectShape.lineTo( 0, rectWidth );
rectShape.lineTo( rectLength, rectWidth );
rectShape.lineTo( rectLength, 0 );
rectShape.lineTo( 0, 0 );

var rectGeom = new THREE.ShapeGeometry( rectShape );
var rectMesh = new THREE.Mesh( rectGeom, new THREE.MeshBasicMaterial( { color: 0xff0000 } ) ) ;

scene.add( rectMesh );
```

#### BoxGeometry（立方几何体）

```js
//width — X轴上的面的宽度.
//height — Y轴上的面的高度.
//depth — Z轴上的面的深度.
//widthSegments — 可选参数. 沿宽度面的分割面数量. 默认值为1.
//heightSegments — 可选参数. 沿高度面的分割面数量. 默认值为1.
//depthSegments — 可选参数. 沿深度面的分割面数量. 默认值为1.
BoxGeometry(width, height, depth, widthSegments, heightSegments, depthSegments)
```

#### SphereGeometry（球几何体）

```js
//radius — 球体半径. 默认值为50.
//widthSegments — 水平分割面的数量. 最小值为3, 默认值为8.
//heightSegments — 垂直分割面的数量. 最小值为2, 默认值为6.
//phiStart — 指定水平起始角度. 默认值为0.
//phiLength — 指定水平扫描角度大小. 默认值为 Math.PI * 2.
//thetaStart — 指定垂直起始角度. 默认值为0.
//thetaLength — 指定垂直扫描角度大小. 默认值为Math.PI.
SphereGeometry(radius, widthSegments, heightSegments, phiStart, phiLength, thetaStart, thetaLength)
```

#### CylinderGeometry（圆柱几何体）

```js
//radiusTop — 圆柱体顶端半径. 默认值为20.
//radiusBottom — 圆柱体底端半径. 默认值为20.
//height — 圆柱体高度. 默认值为100.
//radiusSegments — 围绕圆柱体周长的分割面数量. 默认值为8.
//heightSegments — 沿圆柱体高度的分割面数量. 默认值为1.
//openEnded — 指示圆柱体两端是打开还是覆盖的布尔值. 默认值为false, 意思是覆盖.
//thetaStart — 第一个分割面的开始角度, 默认值 = 0 (3点钟方向).
//thetaLength — 圆形扇形的圆心角通常称为θ。默认为2 * Pi，这形成了一个完整的圆柱体.
CylinderGeometry(radiusTop, radiusBottom, height, radiusSegments, heightSegments, openEnded, thetaStart, thetaLength)
```

#### ConeGeometry（圆锥几何体）

```js
//radius — 锥底半径. 默认值为20.
//height — 锥体高度. 默认值为100.
//radiusSegments — 围绕圆锥周长的分割面数量. 默认值为8.
//heightSegments — 沿圆锥高度的分割面数量. 默认值为1.
//openEnded — 指示锥底是打开还是覆盖的布尔值. 默认值为false, 意思是覆盖.
//thetaStart — 第一个分割面的开始角度, 默认值 = 0 (3点钟方向).
//thetaLength — 圆形扇形的圆心角通常称为θ。默认为2 * Pi，这形成了一个完整的锥体.
ConeGeometry(radius, height, radiusSegments, heightSegments, openEnded, thetaStart, thetaLength)
```

#### TorusGeometry（圆环几何体）

```js
//radius — 半径, 默认值为100.
//tube — 管道直径. 默认值为40.
//radialSegments — 默认值为8
//tubularSegments — 默认值为6.
//arc — 圆心角. 默认值为Math.PI * 2.
TorusGeometry(radius, tube, radialSegments, tubularSegments, arc)
```

#### TetrahedronGeometry（四面几何体，三棱锥）

```js
//radius — 四面体半径. 默认值为1.
//detail — 默认值为0. 设置为大于0的值将添加顶点使之不再是一个四面体.
TetrahedronGeometry(radius, detail)
```

#### OctahedronGeometry（八面几何体，双面三棱锥）

```js
//radius — 八面体半径. 默认值为1.
//detail — 默认值为0. 如果此值设为大于0则不再是八面体.
OctahedronGeometry(radius, detail)
```

#### DodecahedronGeometry（十二面几何体，正五边形十二面体）

```js
//radius — 十二面体的半径. 默认值为1.
//detail — 默认值为0. 设置为大于0的值将添加顶点使之不再是一个十二面体.
DodecahedronGeometry(radius, detail)
```

#### IcosahedronGeometry（二十面几何体，正三边形十二面体）

```js
//radius — 默认值为1.
//detail — 默认值为0. 设置为大于0的值将添加顶点使之不再是一个二十面体. 当值大于1时它就成了一个球体.
IcosahedronGeometry(radius, detail)
```

#### PolyhedronGeometry（多面几何体）

```js
var verticesOfCube = [
    -1,-1,-1,    1,-1,-1,    1, 1,-1,    -1, 1,-1,
    -1,-1, 1,    1,-1, 1,    1, 1, 1,    -1, 1, 1,
];

var indicesOfFaces = [
    2,1,0,    0,3,2,
    0,4,7,    7,3,0,
    0,1,5,    5,4,0,
    1,2,6,    6,5,1,
    2,3,7,    7,6,2,
    4,5,6,    6,7,4
];
//vertices — Array 以 [1,1,1, -1,-1,-1, ... ] 这种形式出现的点的数组
//faces — Array 以 [0,1,2, 2,3,0, ... ] 这种形式出现的构成各个面的指数数组
//radius — Float - 最终形状的半径
//detail — Integer - 把几何模型细分成多少层. 层越多形状越光滑.
//PolyhedronGeometry(vertices, faces, radius, detail)
var geometry = new THREE.PolyhedronGeometry( verticesOfCube, indicesOfFaces, 6, 2 );
```

#### TorusKnotGeometry（圆环扭结几何体）

```js
//radius — 半径, 默认值为100.
//tube — 管道直径. 默认值为40.
//tubularSegments — 默认值为64.
//radialSegments — 默认值为8.
//p — 这个值决定了几何体绕旋转对称轴绕了多少圈. 默认值为2.
//q — 这个值决定了几何体绕环面的圆绕了多少圈. 默认值为3.
TorusKnotGeometry(radius, tube, tubularSegments, radialSegments, p, q)
```

#### TubeGeometry（管道几何体）

```js
var CustomSinCurve = THREE.Curve.create(
    function ( scale ) { //custom curve constructor
        this.scale = (scale === undefined) ? 1 : scale;
    },

    function ( t ) { //getPoint: t is between 0-1
        var tx = t * 3 - 1.5,
            ty = Math.sin( 2 * Math.PI * t ),
            tz = 0;

        return new THREE.Vector3(tx, ty, tz).multiplyScalar(this.scale);
    }
);

var path = new CustomSinCurve( 10 );

var geometry = new THREE.TubeGeometry(
    path,  //path 从 Curve 基本类继承而来的路径
    20,    //segments 组成管道的分割面数量, 默认值为64
    2,     //radius 管道半径, 默认值为1
    8,     //radiusSegments 组成截面的分割面数量, 默认值为8
    false  //closed 管道是开放的还是闭合的, 默认值为false
);
```

#### ExtrudeGeometry（挤压几何体）

将一个2D图形拉伸为一个3D几何体
```js
//shapes — 形状或形状数组.
//options — 包括下面这些参数的对象.
//  curveSegments — int. 曲线上点的个数
//  steps — int. 用于细分拉伸的样条段数量
//  amount — int. 拉伸形状的深度
//  bevelEnabled — bool. 打开斜面
//  bevelThickness — float. 在原来的形状里面弄多深的斜面
//  bevelSize — float. 斜面离形状轮廓的距离
//  bevelSegments — int. 斜面层的数量
//  extrudePath — THREE.CurvePath. 沿3D样条路径拉伸形状. (创建帧（如果帧没有定义))
//  frames — THREE.TubeGeometry.FrenetFrames. 包含切线、法线、副法线的数组
//  material — int. 前面和后面的材质索引号
//  extrudeMaterial — int. 拉伸或斜化面的材质索引号
//  UVGenerator — Object. 提供UV生成器各功能的对象
ExtrudeGeometry(shapes, options)
```

#### LatheGeometry（车削几何体，带洞灯罩）

```js
var points = [];
for ( var i = 0; i < 10; i ++ ) {
points.push( new THREE.Vector2( Math.sin( i * 0.2 ) * 10 + 5, ( i - 5 ) * 2 ) );
}
//points — Vector2s数组. X轴上每个点都必须大于0.
//segments — 生成圆周段的数目. 默认值为12.
//phiStart — 起始角度的弧度值. 默认值为0.
//phiLength — 弧度范围在0到2PI间的，2PI是闭合车床, 小于2PI的是部分。默认值为2PI.
//LatheGeometry(points, segments, phiStart, phiLength)
var geometry = new THREE.LatheGeometry( points );
var material = new THREE.MeshBasicMaterial( { color: 0xffff00 } );
var lathe = new THREE.Mesh( geometry, material );
scene.add( lathe );
```

#### Geometry（自定义几何体）

通过添加属性值得到相应几何体
```js
//点：this.vertices = [];
//颜色：this.colors = [];
//面：this.faces = []
var geometry = new THREE.Geometry();
geometry.vertices.push(
new THREE.Vector3(-100,100,0),
    new THREE.Vector3(100,-100,0),
    new THREE.Vector3(100.-100,0)
);
```

#### ParametricGeometry（参数化几何体）

```js
//func — 一个函数，接收介于0到1之间的 u 和 v 值，并返回一个 Vector3
//slices — 用于参数化函数的切片数量
//stacks — 用于参数化函数的堆栈数量
ParametricGeometry(func, slices, stacks)
```

#### TextGeometry（文本几何体）

```js
//text — 要显示的文字
//parameters — 包含下面这些参数的对象
//  font — THREE. 字体.
//  size — Float. 大小.
//  height — Float. 文字厚度. 默认值为50.
//  curveSegments — Integer. 曲线上点的数量. 默认值为12.
//  bevelEnabled — Boolean. 是否打开斜面. 默认值为False.
//  bevelThickness — Float. 文本斜面的深度. 默认值为10.
//  bevelSize — Float. 斜面离轮廓的距离. 默认值为8.
TextGeometry(text, parameters)
```

### 灯光（light）

3d引擎在没有手动创建光的情况下会默认有个环境光，不然你什么都看不到。常见的灯光有以下几种类型:

#### AmbientLight（环境光，没有方向全局打亮，不会产生明暗）

不能将 THREE.AmbientLight 作为场景中唯一的光源，因为它会将场景中的所有物体渲染为相同的颜色，而不管是什么形状。

在使用其他光源（如 THREE.SpotLight 或者 THREE.DirectionLight）的同时使用它，目的是弱化阴影或给场景添加一些额外的颜色。

```js
var ambientLight = new THREE.AmbientLight(0x523318);
scene.add(ambientLight);
```

#### DirectionLight（平行光，无衰减，参考日光来理解）

```js
//THREE.DirectionalLight(hex,intensity)
//hex：光的颜色，用16进制表示
//intensity：光线的强度，默认为1。因为RGB的三个值均在0-255之间，不能反映出光照的强度变化，光照越强，物体表面就更明亮。它的取值范围是0-1.如果为0，表示光线基本没有什么作用，那么物体就会显示会黑色。
//平行光的方向：方向由位置和原点（0,0,0）来决定，方向光只与方向有关，与离物体的远近无关。
var light = new THREE.DirectionalLight(0xff0000,1);
light.position.set(0,0,1);
scene.add(light);
```

#### PointLight（点光源，参考灯泡来理解）

```js
//PointLight(color,intensity,distance)
var pointLight = new THREE.PointLight("#ccffcc");
pointLight.position.set(0,10,10);
scene.add(pointLight);
//color：光源的颜色
//distance：光源照射的距离。默认值为 0，意味着光的强度不会随着距离的增加而减少。
//intensity：光源照射的强度。默认值为 1。
//position：光源在场景中的位置。
//visible：设为 ture（默认值），光源就会打开。设为 false，光源就会关闭。
```

#### SpotLight（聚光灯，有衰减，参考舞台聚光灯）

```js
THREE.SpotLight(hex,intensity,distance,angle,exponent)
//hex：聚光灯发出的颜色，十六进制。
//intensity：光源的强度。默认是1.0，如果为0.5，则强度是一半，意思是颜色会淡一些。和点光源一样。
//distance：光线的强度，从最大值衰减到0需要的距离。默认为0，表示光不衰减，如果非0，则表示从光源的位置到Distance的距离，光都在线性衰减。到离光源距离distance时，光源强度为0
//angle：聚光灯着色的角度，用弧度作为单位，这个角度是和光源的方向形成的角度。
//exponent：光源模型中，衰减的一个参数，越大衰减越快
```

### 纹理（texture）

纹理可以看作是图片，或者贴图。3d世界的纹理由图片组成。

```js
//image：这是一个图片的类型，基本上由 ImageUtils来加载
    //var image = THREE.ImageUtils.loadTexture(url);
    //url不能加载本地图片
    //加载的图片的大小必须是2的次方
//mapping：是一个THREE.UVMapping()类型，表示的是纹理坐标。
//wrapS：表示x轴的纹理的回环方式，就是当纹理的宽度小于需要贴图的平面的宽度时，平面剩下的部分应该以何种方式贴图的问题。
//wrapT：表示y轴的纹理回环方式。mapFilter和minFilter表示过滤的方式，这是OpenGL的基本概念。不设置时会取默认值。
//format：表示加载图片的格式，这个参数可以取值THREE.RGBAFormat,RGBFormat等。
    //THREE.RGBAFormat表示每个像素点要使用四个分量表示，分别是红、绿、蓝、透明表示。
    //RGBFormat表示不适用透明，也就是说纹理不会又透明的效果。
//type：表示存储纹理额的内存的每一个字节的格式，是有符号还是没有符号；是整形还是浮点型。默认是无符号型。
//anisotropy：各向异性过滤。使用各向异性过滤能够使纹理的效果更好，但是会消耗更多的内存、CPU、GPU时间。
THREE.Texture (image,mapping,wrapS,wrapT,magFilter,minFilter,format,type,anisotropy)
```

* 纹理的坐标

    (0,0)在左下，向右上递增，用一幅图来做纹理的时候，要逆时针指定4角坐标

* 重复纹理的方式(回环)

    * 简单重复：THREE.RepeatWrapping;纹理将重复无限远。
    * 边缘拉伸：THREE.ClampToEdgeWrappinng，这个是默认设置。即纹理事务最后一个像素延伸到网格的边缘。
    * 镜像重复：THREE.MirroredRepeatWrapping，将纹理重复到无穷大，并在每次重复时都进行镜像。

### 贴图（texture）

想象一下你手里有一个立方体，你用一张A4纸包裹上立方体的所有面，并在上面画画。你画的内容就是贴图。

1. 普通贴图（_col）:material.map，替代颜色

2. 法线贴图（_nor）:material.normalMap，让细节程度较低的表面生成高细节程度的精确光照方向和反射效果

3. 环境光遮蔽贴图（_occ）:material.aoMap，用来描绘物体和物体相交或靠近的时候遮挡周围漫反射光线的效果

4. 环境反射贴图:material.envMap，用于模拟材质反射周围环境的效果

贴图文件统一加载到内存
```js
var allTexture;
function loadAllTexture(cb){
    allTexture = {};

    var loadIndex = 0;
    var textures = [
        "skymap",
        "shache_occ",
        "shache_nor",
        "shache_col",
        "neishi_occ",
        "neishi_nor",
        "mennei_col",
        "luntai_nor",
        "luntai_col",
        "lungu_occ",
        "lungu_nor",
        "lungu_col",
        "linjian_occ",
        "linjian_nor",
        "linjian_col",
        "floor",
        "deng_occ",
        "deng_nor",
        "deng_col",
        "cheshen_occ",
        "cheshen_nor",
        "chejia_occ",
        "chejia_nor",
        "chedengzhao_nor"
    ];

    function loadNextTexture(){
        var textureName = textures[loadIndex];
        loadTexture("images/textures/"+textureName+".jpg",function(texture){
            if(loadIndex<textures.length-1){
                allTexture[textureName] = {
                    texture:texture
                };

                loadIndex++;
                loadNextTexture();
            }else{
                if(cb)cb();
            }
        });
    }
    loadNextTexture();
}
function loadTexture(filepath,cb){
    const textureLoader = new THREE.TextureLoader();
    textureLoader.load(filepath,cb);
}
```

根据名称手动一一对应
```js
for(var i=0;i<gltf.scene.children[0].children.length;i++){
    var modelObj = gltf.scene.children[0].children[i];

    if(modelObj.name=="smart_lungu0"||modelObj.name=="smart_lungu1"||modelObj.name=="smart_lungu2"||modelObj.name=="smart_lungu3"){
        modelObj.material = new THREE.MeshStandardMaterial();
        modelObj.material.map = allTexture["lungu_col"].texture;
        modelObj.material.normalMap = allTexture["lungu_nor"].texture;
        modelObj.material.aoMap = allTexture["lungu_occ"].texture;
    }
}
```

### 材质（material）

延续贴图里的想象，你用白卡纸画画，还是用油纸画画，呈现出来的质感是不同

1. MeshBasicMaterial（基础材质，不受光照影响）
2. MeshStandardMaterial（PBR标准材质）
3. MeshPhongMaterial（高光材质，适用于陶瓷，烤漆类质感）
4. MeshToonMaterial（卡通材质，俗称三渲二）
5. MeshStandardMaterial（PBR标准材质模拟金属反射）

* 样例

    * 透明的玻璃

    天窗和前挡风玻璃的透明度以及基底颜色是不同的
    ```js
    else if(child.name=="smart_boli"){
        child.material=new THREE.MeshPhongMaterial();
        child.material.color = new THREE.Color( 0x333333 );
        child.material.transparent=true;
        child.material.opacity=.2;
    }else if(child.name=="smart_tianchuang"){
        child.material=new THREE.MeshPhongMaterial();
        child.material.color = new THREE.Color( 0x000 );
        child.material.transparent=true;
        child.material.opacity=.5;
    }
    ```

    * 玻璃的反射

    ```js
    child.material.envMap=allTexture["skymap"].texture;
    //环境反射贴图envMap的映射方式，这里用的是一个叫等量矩形投影的映射方法
    child.material.envMap.mapping = THREE.EquirectangularReflectionMapping;
    //环境反射贴图的强度
    child.material.envMapIntensity=1;
    ```

    * 车身漆面质感

    使用MeshStandardMaterial材质，通过调节metalness，roughness的值来调节金属的质感
    ```js
    child.material = new THREE.MeshStandardMaterial();
                        
    child.material.color=new THREE.Color(0x70631B);
    child.material.metalness = 0.44;
    child.material.roughness = 0;
    ```

### 3d模型的文件格式

1. OBJ格式

    老牌通用3d模型文件，不包含贴图，材质，动画等信息。

2. GLTF格式（图形语言传输格式）

    由OpenGL官方维护团队推出的现代3d模型通用格式，可以包含几何体、材质、动画及场景、摄影机等信息，并且文件量还小。有3D模型界的JPEG之称。

    ```js
    //<script src="js/GLTFLoader.js"></script>
    //放到之前添加立方体的代码处
    const loader = new THREE.GLTFLoader();

    //加载一个.gltf格式的3d模型文件
    loader.load(
        'images/model.gltf',
        function ( gltf ) {
            scene.add( gltf.scene );
        },
        function ( xhr ) {
            //侦听模型加载进度
            console.log( ( xhr.loaded / xhr.total * 100 ) + '% loaded' );
        },
        function ( error ) {
            //加载出错时的回调
            console.log( 'An error happened' );
        }
    );

    //遍历查看模型里的几何体列表
    //console.log(gltf.scene.children);
    //可以用for，也可以用traverse api
    //gltf.scene.children.traverse((child){});
    ```

### 信息点

物体定位:需通过坐标器手动计算

```js
Raycaster( origin, direction, near, far ) 

//origin — 射线的起点向量。
//direction — 射线的方向向量，应该归一标准化。
//near — 所有返回的结果应该比 near 远。Near不能为负，默认值为0。
//far — 所有返回的结果应该比 far 近。Far 不能小于 near，默认值为无穷大。
```

推导过程
```txt
mouse.x = (e.clientX / window.innerWidth) * 2 - 1;
mouse.y = -(e.clientY / window.innerHeight) * 2 + 1;
    
推导过程：
设A点为点击点(x1,y1),x1=e.clintX, y1=e.clientY，原点在左上角，右x正半轴，下y正半轴
设A点在世界坐标中的坐标值为B(x2,y2)，原点在屏幕中心，右x正半轴，上y正半轴
A需要通过翻折平移等方法，求出相同位置不同坐标系对应坐标
先将坐标方向对齐：A的屏幕(第一象限)实际在B的第四象限，x不变，y翻折(x1,-y1)
然后x和y均需平移半个屏幕
x2' = x1 - innerWidth/2
y2' = innerHeight/2 - y1
又由于在世界坐标的范围是[-1,1],要得到正确的B值我们必须要将坐标标准化
x2 = (x1 -innerWidth/2)/(innerwidth/2) = (x1/innerWidth)*2-1
同理得 y2 = -(y1/innerHeight)*2 +1
```

Sprite+Raycast
```js
//frame只是一个标记，叫什么都行
var poiPosArray=[
    {x:-1.47,y:0.87,z:-0.36,frame:1},
    {x:-1.46,y:0.49,z:-0.69,frame:2},
    {x:1.5,y:.7,z:0,frame:8},
    {x:0.33,y:1.79,z:0,frame:3},
    {x:0,y:0.23,z:0.96,frame:4},
    {x:0.73,y:1.38,z:-0.8,frame:5},
    {x:-.1,y:1.17,z:0.88,frame:6},
    {x:-1.16,y:0.16,z:0.89,frame:7}
],poiObjects=[];
function setupInfoPoint(){
    const pointTexture = new THREE.TextureLoader().load("images/point.png");

    var group = new THREE.Group();
    var materialC = new THREE.SpriteMaterial( { map: pointTexture, color: 0xffffff, fog: false } );
    for ( var a = 0; a < poiPosArray.length; a ++ ) {
        var x = poiPosArray[a].x;
        var y = poiPosArray[a].y-.5;
        var z = poiPosArray[a].z;

        var sprite = new THREE.Sprite( materialC );
        sprite.scale.set( .15, .15, 1 );
        sprite.position.set( x, y, z );
        sprite.idstr="popup_"+poiPosArray[a].frame;
        group.add( sprite );

        poiObjects.push(sprite);
    }
    scene.add( group );

    document.body.addEventListener("click",function (event) {
        event.preventDefault();

        var raycaster = new THREE.Raycaster();
        var mouse = new THREE.Vector2();
        mouse.x = ( event.clientX / window.innerWidth ) * 2 - 1;
        mouse.y = - ( event.clientY / window.innerHeight ) * 2 + 1;

        raycaster.setFromCamera( mouse, camera );

        var intersects = raycaster.intersectObjects( poiObjects );
        if(intersects.length>0){
            var popIndex=parseInt(intersects[ 0 ].object.idstr.substr(6,1));
            console.log(popIndex);
        }
    });
}
```

### 性能监视器Stats

* 概念

    * FPS：表示上一秒的帧数，值越大越好，一般为60左右。点击下图会变成绿色的。
    * MS：表示渲染一帧需要的毫秒数，这个数字越小越好。再次点击可回到FPS视图中。

* stats

    ```js
    var stats = new Stats();
    stats.setMode(1) //参数为0时，FPS界面。参数为1时，MS界面。参数为2时，内存界面。其它为自定义界面
    //将Stats的界面放在左上角
    stats.domElement.style.position = 'absolute';
    stats.domElement.style.left = '0px';
    stats.domElement.style.top = '0px';
    document.body.appendChild(stats.domElement);
    setInterval(function(){
        //在要测试的代码前面调用begin函数，在代码执行完毕后调用end函数，这样就能统计出这段代码执行的平均帧数了。
        stats.begin();
        //每一帧代码stats.update()
        stats.end();
    },1000/60);
    ```

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>让物体动起来</title>
        <script src="three.js"></script>
        <script src="stats.js"></script>
    </head>
    <body>
        <div id='app'></div>
        <script>
            //创建场景
            var scene = new THREE.Scene();
            //创建相机
            var camera = new THREE.PerspectiveCamera(105,window.innerWidth/window.innerHeight,1,1000);
            camera.position.x = 0;
            camera.position.y = 0;
            camera.position.z = 40;
            //创建渲染器
            render = new THREE.WebGLRenderer({
                antialias:true
            });
            //设置画布大小
            render.setSize(window.innerWidth,window.innerHeight);

            var app = document.getElementById("app");
            app.appendChild(render.domElement);

            //创造一个立方体，点模型
            var geometry = new THREE.CylinderGeometry(10,20,15,5);//参数：顶面半径，地面半径，高度，分成几边体
            //创造一个立方体，网格模型
            var material3 = new THREE.MeshBasicMaterial({
                color:0x00ff00
            });
            var meshs = new THREE.Mesh(geometry,material3);
            //创建物体的边框线
            var geoedg = new THREE.EdgesGeometry(geometry,10);
            var edgcol = new THREE.LineBasicMaterial({color:0xffd700});
            var geoline = new THREE.LineSegments(geoedg,edgcol);

            meshs.add(geoline);
            scene.add(meshs);

            //渲染
            render.render(scene,camera);

            //性能监视器
            var stats = new Stats();
            stats.setMode(0);
            stats.domElement.style.position = 'absolute';
            stats.domElement.style.left = '30px';
            stats.domElement.style.top = '10px';
            app.appendChild(stats.domElement);

            //产生动画
            function animate(){
                //相机移动
                camera.position.y -=0.05;
                if(camera.position.y < -10){
                    camera.position.z +=0.05;
                }

                render.render(scene,camera);

                //物体移动
                //meshs.position.y +=0.05;
                //if(meshs.position.y>10){
                    //meshs.position.z -=0.05;
                //}
                //render.render(scene,camera);
                //window.requestAnimationFrame(animate);
                stats.update();
            }
            setInterval(animate,10);

        </script>
    </body>
    </html>
    ```

### 平台

模型:sketchfab
编辑器:[threejs editor](https://threejs.org/editor/)

### 优化

在移动端网页里流畅运行，最多不能超过10万面

### 样例

#### 球形3D漫游

[官方示例效果](https://threejs.org/examples/?q=webgl_panorama_equirectangular#webgl_panorama_equirectangular)

1. 思路

    * 第一步：构建一个空间直角坐标系 ：Three中称之为场景(Scene)
    * 第二步：在坐标系中，绘制几何体： Three中的几何体有很多种，包括BoxGeometry（立方体），SphereGeometry（球体）等等
    * 第三步：选择一个观察点，并确定观察方向等：Three中称之为相机(Camera)
    * 第四步：将观察到的场景渲染到屏幕上的指定区域 ：Three中使用Renderer完成这一工作（相当于拍照）

2. 素材

球体全景所需的图片素材：宽是高的两倍，数值是2的整数倍最好，建议图片宽高为2048px*1024px

3. 理论基础

```txt
经度：lon，取值范围：[0,360]，纬度：lat，取值范围：[-90,90];

经纬度转换三维坐标

X = R * cos(lat)* sin(lon)
Y = R * sin(lat)
Z = R * cos(lat)*cos(lon)

ThreeJS中默认的坐标系是右手坐标系，X轴为左右，Y轴为上下，Z轴为前后。
```

4. 具体步骤

* 第一步：创建一个场景（Scene）
* 第二步：创建一个球体，并将全景图片贴到球体的内表面，放入场景中
* 第三步：创建一个透视投影相机将camera拉到球体的中心，相机观看球体内表面
* 第四步：通过修改经纬度来，改变相机观察的点

5. 样例代码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>手把手教你制作酷炫Web全景</title>
    <meta name="viewport" id="viewport" content="width=device-width,initial-scale=1,minimum-scale=1, maximum-scale=1, user-scalable=no, viewport-fit=cover">
</head>
<body>
    <div id="wrap" style="position: absolute;z-index: 0;top: 0;bottom: 0;left: 0;right: 0;width: 100%;height: 100%;overflow: hidden;">
    </div>
    <script src="https://cdn.bootcdn.net/ajax/libs/three.js/r128/three.js"></script>
    <script>
        const width = window.innerWidth, height = window.innerHeight // 屏幕宽高
        const radius = 50 // 球体半径

        // 第一步：创建场景
        const scene = new THREE.Scene()

        // 第二步：绘制一个球体
        const geometry = new THREE.SphereBufferGeometry(radius, 32, 32)
        geometry.scale(-1, 1, 1) // 球面反转，由外表面改成内表面贴图
        const material = new THREE.MeshBasicMaterial({
            map: new THREE.TextureLoader().load('./img/1.jpeg') // 上面的全景图片
        })
        const mesh = new THREE.Mesh(geometry, material)
        scene.add(mesh)

        // 第三步：创建相机，并确定相机位置
        const camera = new THREE.PerspectiveCamera(75, width / height, 0.1, 100)
        camera.position.x = 0  // 确定相机位置移到球心
        camera.position.y = 0
        camera.position.z = 0

        camera.target = new THREE.Vector3(radius, 0, 0) // 设置一个对焦点
        

        // 第四步：拍照并绘制到canvas
        const renderer = new THREE.WebGLRenderer()
        renderer.setPixelRatio(window.devicePixelRatio)
        renderer.setSize(width, height) // 设置照片大小

        document.querySelector('#wrap').appendChild(renderer.domElement) // 绘制到canvas
        renderer.render(scene, camera)

        let lat = 0, lon = 0

        function render() {
            lon += 0.003 // 每帧加一个偏移量
            // 改变相机的对焦点，计算公式参考：2.2.2章节
            camera.target.x = radius * Math.cos(lat) * Math.cos(lon);
            camera.target.y = radius * Math.sin(lat);
            camera.target.z = radius * Math.cos(lat) * Math.sin(lon)
            camera.lookAt(camera.target) // 对焦

            renderer.render(scene, camera)
            requestAnimationFrame(render)
        }
        render()
    </script>
</body>

</html>
```

6. 手指在屏幕滑动过程

* touchstart：记录滑动起始的位置（startX，startY, startTime）
* touchmove：记录当前位置（curX，curY）相减上一次位置的值，乘以factor，计算出（lon，lat），【触摸跟随】
* touchend：记录endTime,计算本次滑动过程中的平均速度，然后，每帧减去减速度d，直至速度为0或者touchstart事件被触发 【触摸结束触发惯性动画】

```js
distanceX = clientX1 - clientX2   // X轴方向
distanceY = clientY1 - clientY2   // Y轴方向

// 其中R为球体半径，根据弧长公式：
lon = distanX / R
lat = distanY / R
```
```js
// 增加touch事件监听
let lastX, lastY       // 上次屏幕位置
let curX, curY         // 当前屏幕位置
const factor = 1 / 10  // 灵敏系数

const $wrap = document.querySelector('#wrap')
// 触摸开始
$wrap.addEventListener('touchstart', function (evt) {
    const obj = evt.targetTouches[0] // 选择第一个触摸点
    startX = lastX = obj.clientX
    startY = lastY = obj.clientY
})

// 触摸中
$wrap.addEventListener('touchmove', function (evt) {
    evt.preventDefault()
    const obj = evt.targetTouches[0]
    curX = obj.clientX
    curY = obj.clientY

    // 参考：弧长公式
    lon -= ((curX - lastX) / radius) * factor // factor为了全景旋转平稳，乘以一个灵敏系数
    lat += ((curY - lastY) / radius) * factor

    lastX = curX
    lastY = curY
})
```

7. 手势缩放

```txt
const camera = new THREE.PerspectiveCamera( fov , aspect , near , fear )
near：取默认值：0.1即可
fear：只要大于球体半径就可，取值为：球体半径R
aspect：在全景的场景已经确定了，照片的长宽比：屏幕宽度 / 屏幕高度
fov：视场，缩放是通过修改它的值来完成全景图片的缩放；
```
```js
// 其中，（clientX1，clientY1）和（clientX2，clientY2）为双指在屏幕的当前位置

// 计算距离，简化运输不用平方计算
const distance = Math.abs(clientX1 - clientX2) + Math.abc(clientY1 - clientY)
// 计算缩放比
const scale = distance / lastDiance 
// 计算新的视角
fov = camera.fov / scale

// 视角范围取值
camera.fov = Math.min(90, Math.max(fov,60)) // 90 > fov > 60 ,从参数说明中选取

// 视角需要主动更新
camera.updateProjectionMatrix()
```

#### 立方体3D漫游

[官方示例效果](https://threejs.org/examples/?q=webgl_panorama_cube#webgl_panorama_cube)

1. 思路

    * 创建黑色场景
    * 创建六面体/球体并贴图
    * 视角(相机)移到空间
    * 添加信息点和点击热点事件

2. 实现

    * 创建黑色场景

        ```js
        var scene, camera, renderer;

        function initThree(){
            //场景
            scene = new THREE.Scene();
            //镜头
            camera = new THREE.PerspectiveCamera(90, document.body.clientWidth / document.body.clientHeight, 0.1, 100);
            camera.position.set(0, 0, 0.01);
            //渲染器
            renderer = new THREE.WebGLRenderer();
            renderer.setSize(document.body.clientWidth, document.body.clientHeight);
            document.getElementById("container").appendChild(renderer.domElement);
            //镜头控制器
            var controls = new THREE.OrbitControls(camera, renderer.domElement);
            
            //一会儿在这里添加3D物体

            loop();
        }

        //帧同步重绘
        function loop() {
            requestAnimationFrame(loop);
            renderer.render(scene, camera);
        }

        window.onload = initThree;
        ```

    * 使用立方体（box）实现

        ```js
        var materials = [];
        //根据左右上下前后的顺序构建六个面的材质集
        var texture_left = new THREE.TextureLoader().load( './images/scene_left.jpeg' );
        materials.push( new THREE.MeshBasicMaterial( { map: texture_left} ) );

        var texture_right = new THREE.TextureLoader().load( './images/scene_right.jpeg' );
        materials.push( new THREE.MeshBasicMaterial( { map: texture_right} ) );

        var texture_top = new THREE.TextureLoader().load( './images/scene_top.jpeg' );
        materials.push( new THREE.MeshBasicMaterial( { map: texture_top} ) );

        var texture_bottom = new THREE.TextureLoader().load( './images/scene_bottom.jpeg' );
        materials.push( new THREE.MeshBasicMaterial( { map: texture_bottom} ) );

        var texture_front = new THREE.TextureLoader().load( './images/scene_front.jpeg' );
        materials.push( new THREE.MeshBasicMaterial( { map: texture_front} ) );

        var texture_back = new THREE.TextureLoader().load( './images/scene_back.jpeg' );
        materials.push( new THREE.MeshBasicMaterial( { map: texture_back} ) );

        var box = new THREE.Mesh( new THREE.BoxGeometry( 1, 1, 1 ), materials );
        scene.add(box);
        ```

    * 使用球体（sphere）实现

        ```js
        var sphereGeometry = new THREE.SphereGeometry(/*半径*/1, /*垂直节点数量*/50, /*水平节点数量*/50);//节点数量越大，需要计算的三角形就越多，影响性能

        var sphere = new THREE.Mesh(sphereGeometry);
        sphere.material.wireframe  = true;//用线框模式大家可以看得清楚是个球体而不是圆形
        scene.add(sphere);

        var texture = new THREE.TextureLoader().load('./images/scene.jpeg');
        var sphereMaterial = new THREE.MeshBasicMaterial({map: texture});

        var sphere = new THREE.Mesh(sphereGeometry,sphereMaterial);
        // sphere.material.wireframe  = true;
        ```

    * 视角(相机)移到立方体

        ```js
        box.geometry.scale( 1, 1, -1 );
        ```

    * 视角(相机)移到球体

        ```js
        var sphereGeometry = new THREE.SphereGeometry(/*半径*/1, 50, 50);
        sphereGeometry.scale(1, 1, -1);
        ```

    * 添加信息点

        点的数组
        ```js
        var hotPoints=[
            {
                position:{
                    x:0,
                    y:0,
                    z:-0.2
                },
                detail:{
                    "title":"信息点1"
                }
            },
            {
                position:{
                    x:-0.2,
                    y:-0.05,
                    z:0.2
                },
                detail:{
                    "title":"信息点2"
                }
            }
        ];
        ```

        遍历这个数组，并将信息点的指示图添加到3D场景中
        ```js
        var pointTexture = new THREE.TextureLoader().load('images/hot.png');
        var material = new THREE.SpriteMaterial( { map: pointTexture} );

        for(var i=0;i<hotPoints.length;i++){
            var sprite = new THREE.Sprite( material );
            sprite.scale.set( 0.1, 0.1, 0.1 );
            sprite.position.set( hotPoints[i].position.x, hotPoints[i].position.y, hotPoints[i].position.z );

        scene.add( sprite );
        }
        ```

    * 点击热点事件

        ```js
        sprite.detail = hotPoints[i].detail;
        poiObjects.push(sprite);
        ```

        通过射线检测（raycast），就像是镜头中心向鼠标所点击的方向发射出一颗子弹，去检查这个子弹最终会打中哪些物体
        ```js
        document.querySelector("#container").addEventListener("click",function(event){
            event.preventDefault();

            var raycaster = new THREE.Raycaster();
            var mouse = new THREE.Vector2();

            mouse.x = ( event.clientX / document.body.clientWidth ) * 2 - 1;
            mouse.y = - ( event.clientY / document.body.clientHeight ) * 2 + 1;

            raycaster.setFromCamera( mouse, camera );

            var intersects = raycaster.intersectObjects( poiObjects );
            if(intersects.length>0){
                alert("点击了热点"+intersects[0].object.detail.title);
            }
        });
        ```

## 更加轻量的3D引擎(css3d)

好处除了库很小以外，还是div+css来搭建三维场景的。但这个库的作者几乎不维护，遇到问题必须得自己想办法解决，比如使用在电脑上会看到明显的面片边缘，但是在手机上浏览的话表现还是相当完美的

使用skybox实现
```js
window.onload=initCSS3D;

function initCSS3D(){
    var s = new C3D.Stage();
    s.size(window.innerWidth, window.innerHeight).update();
    document.getElementById('container').appendChild(s.el);

    var box = new C3D.Skybox();
    box.size(954).position(0, 0, 0).material({
        front: {image: "images/scene_front.jpeg"},
        back: {image: "images/scene_back.jpeg"},
        left: {image: "images/scene_right.jpeg"},
        right: {image: "images/scene_left.jpeg"},
        up: {image: "images/scene_top.jpeg"},
        down: {image: "images/scene_bottom.jpeg"},

    }).update();
    s.addChild(box);

    function loop() {
        angleX += (curMouseX - lastMouseX + lastAngleX - angleX) * 0.3;
        angleY += (curMouseY - lastMouseY + lastAngleY - angleY) * 0.3;

        s.camera.rotation(angleY, -angleX, 0).updateT();
        requestAnimationFrame(loop);
    }

    loop();

    var lastMouseX = 0;
    var lastMouseY = 0;
    var curMouseX = 0;
    var curMouseY = 0;
    var lastAngleX = 0;
    var lastAngleY = 0;
    var angleX = 0;
    var angleY = 0;

    document.addEventListener("mousedown", mouseDownHandler);
    document.addEventListener("mouseup", mouseUpHandler);

    function mouseDownHandler(evt) {
        lastMouseX = curMouseX = evt.pageX;
        lastMouseY = curMouseY = evt.pageY;
        lastAngleX = angleX;
        lastAngleY = angleY;

        document.addEventListener("mousemove", mouseMoveHandler);
    }

    function mouseMoveHandler(evt) {
        curMouseX = evt.pageX;
        curMouseY = evt.pageY;
    }

    function mouseUpHandler(evt) {
        curMouseX = evt.pageX;
        curMouseY = evt.pageY;

        document.removeEventListener("mousemove", mouseMoveHandler);
    }
}
```

添加信息点
```js
var hotPoints=[
    {
        position:{
            x:0,
            y:0,
            z:-476
        },
        detail:{
            "title":"信息点1"
        }
    },
    {
        position:{
            x:0,
            y:0,
            z:476
        },
        detail:{
            "title":"信息点2"
        }
    }
];
function initPoints(){
    var poiObjects = [];
    for(var i=0;i<hotPoints.length;i++){
        var _p = new C3D.Plane();

        _p.size(207, 162).position(hotPoints[i].position.x,hotPoints[i].position.y,hotPoints[i].position.z).material({
            image: "images/hot.png",
            repeat: 'no-repeat',
            bothsides: true,//注意这个两面贴图的属性
        }).update();
        s.addChild(_p);

        _p.el.detail = hotPoints[i].detail;

        _p.on("click",function(e){
            console.log(e.target.detail.title);
        })
    }
}
```

bothsides属性为true时，背面的信息点图片是反的。需根据其与相机的夹角重置一下信息点的旋转角度。
```js
var r = Math.atan2(hotPoints[i].position.z-0,0-0) * 180 / Math.PI+90;
_p.size(207, 162).position(hotPoints[i].position.x,hotPoints[i].position.y,hotPoints[i].position.z).material({
            image: "images/hot.png",
            repeat: 'no-repeat',
            bothsides: false,
        }).update();
```
