# as1

```
在上次作业中，虽然我们在屏幕上画出一个线框三角形，但这看起来并不是那么的有趣。
所以这一次我们继续推进一步——在屏幕上画出一个实心三角形，换言之，栅格化一个三角形。上一次作业中，在视口变化之后，我们调用了函数 rasterize_wireframe(const Triangle& t)。
但这一次，你需要自己填写并调用函数 rasterize_triangle(const Triangle& t)。
该函数的内部工作流程如下:
1. 创建三角形的 2 维 bounding box。
2. 遍历此 bounding box 内的所有像素（使用其整数索引）。然后，使用像素中心的屏幕空间坐标来检查中心点是否在三角形内。
3. 如果在内部，则将其位置处的插值深度值 (interpolated depth value) 与深度缓冲区 (depth buffer) 中的相应值进行比较。
4. 如果当前点更靠近相机，请设置像素颜色并更新深度缓冲区 (depth buffer)。
你需要修改的函数如下:
• rasterize_triangle(): 执行三角形栅格化算法
• static bool insideTriangle(): 测试点是否在三角形内。你可以修改此函数的定义，这意味着，你可以按照自己的方式更新返回类型或函数参数。
因为我们只知道三角形三个顶点处的深度值，所以对于三角形内部的像素，我们需要用插值的方法得到其深度值。我们已经为你处理好了这一部分，因为有关这方面的内容尚未在课程中涉及。插值的深度值被储存在变量 z_interpolated中。
```

## Run

```shell
$ mkdir build
$ cd build
```

```shell
$ cmake ..
$ make
```

```c++
./Rasterizer
```
