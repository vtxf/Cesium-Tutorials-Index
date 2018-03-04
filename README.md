# Cesium相关资料汇总

https://github.com/vtxf/Cesium-Tutorials-Index  
Cesium是一个用于显示三维地球和地图的开源js库。  
官网地址：https://cesiumjs.org/ 。  
它可以用来显示海量三维模型数据、影像数据、地形高程数据、矢量数据等等。三维模型格式支持gltf、三维瓦片模型格式支持3d-tilse。矢量数据支持geojson、topojson格式。影像数据支持wmts等。高程支持STK格式。  
Cesium每月出一个版本，目前（2018/3/4）最新版是：1.43。下载地址：https://cesiumjs.org/downloads/   
## 教程汇总
### Cesium官方教程
教程集合：https://cesiumjs.org/tutorials/  
API文档：https://cesiumjs.org/refdoc/  
示例程序：https://cesiumjs.org/Cesium/Build/Apps/Sandcastle/   
github地址：https://github.com/AnalyticalGraphicsInc/cesium.git   
Cesium官网国内访问较慢，可以在github上下载源码或者zip包来开发，其中已包含示例和API文档。
### Peter Lu的Cesium教程汇总 
http://www.cnblogs.com/fuckgiser/p/5706842.html  
Cesium应用篇：1快速搭建 http://www.cnblogs.com/fuckgiser/p/5633748.html  
Cesium应用篇：2影像服务（上） http://www.cnblogs.com/fuckgiser/p/5647429.html  
Cesium应用篇：2影像服务（下） http://www.cnblogs.com/fuckgiser/p/5647457.html  
Cesium应用篇：3控件（1）Clock http://www.cnblogs.com/fuckgiser/p/5669920.html  
Cesium应用篇：3控件（2）BaseLayerPicker http://www.cnblogs.com/fuckgiser/p/5686238.html  
Cesium应用篇：3控件（3）SelectionIndicator& InfoBox http://www.cnblogs.com/fuckgiser/p/5702544.html  
Cesium应用篇：3控件（4）Geocoder http://www.cnblogs.com/fuckgiser/p/5708673.html  
Cesium应用篇：3控件（5）CesiumInspector http://www.cnblogs.com/fuckgiser/p/5715342.html  
Cesium应用篇：3控件（6） FullScreen/ VR / Home http://www.cnblogs.com/fuckgiser/p/5716046.html  
### 合肥火星科技
快速入门：http://www.marsgis.cn/cesium/docs/go.html?id=11  
翻译的Cesium教程：http://www.marsgis.cn/cesium/docs/go.html?id=12  
## 工具汇总
### gltf相关
Cesium加载模型时使用gltf格式。gltf格式是opengl官方的三维模型格式，充分考虑了网络模式下数据加载的特点，非常适合网络环境下使用。gltf目前已有1.0和2.0两个版本，Cesium从1.36版开始同时支持gltf1.0和支持gltf2.0格式。
#### gltf
https://github.com/KhronosGroup/glTF  
gltf规格说明  
#### glTF-Sample-Models
https://github.com/KhronosGroup/glTF-Sample-Models
gltf样例数据  
#### gltf-pipeline
https://github.com/AnalyticalGraphicsInc/gltf-pipeline  
用来处理gltf格式文件，主要功能有： 
* 将gltf格式分解成多个文件（纹理、顶点二进制数据、shader等）
* 文本格式(gltf)和二进制格式(glb)的互转
* 将纹理压缩成dds、pvr、etc等分别适合windows桌面端、iphone手机端、android手机端纹理的高效显示
* 自动进行纹理烘焙，生成环境遮蔽纹理(ambient occlusion)
* 对顶点数据进行压缩等
#### gltf-vscode
https://github.com/AnalyticalGraphicsInc/gltf-vscode  
vscode插件，可以在vscode中打开gltf文件的同时显示三维模型。  
#### obj2gltf
https://github.com/AnalyticalGraphicsInc/obj2gltf  
将obj格式模型转成gltf格式模型  
### 3d-tiles相关
3d-tiles是Cesium用来显示大规模海量三维模型数据格式，比如倾斜摄影数据，可以通过转化成3d-tiles格式来在Cesium中显示出来。3d-tiles格式考虑了普通三维模型、点云数据、矢量数据等形式，其中矢量数据格式还在开发中，目前的源码中已经有体现，但是官方还未做宣传；普通三维模型等格式已相对成熟。3d-tiles内部实际上是使用gltf来作为单个瓦片模型的格式。
#### 3d-tiles
https://github.com/AnalyticalGraphicsInc/3d-tiles
3d-tiles格式标准
#### 3d-tiles-tools
https://github.com/AnalyticalGraphicsInc/3d-tiles-tools
3d-tiles格式处理工具，可以对3d-tiles进行调试、分析、验证。
#### 3d-tiles-samples
https://github.com/AnalyticalGraphicsInc/3d-tiles-samples
3d-tiles的样例数据

### 其他杂项
#### cesium-threejs-experiment
https://github.com/AnalyticalGraphicsInc/cesium-threejs-experiment  
同时使用Cesium和three.js进行三维展示
#### quantized-mesh
https://github.com/AnalyticalGraphicsInc/quantized-mesh  
Cesium所使用的STK地形格式标准
