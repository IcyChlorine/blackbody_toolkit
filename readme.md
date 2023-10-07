 

# Basic Blackbody Radiation Toolkit

![sun_and_earth](C:\StarSky\Programming\MyProjects\blackbody_toolkit\sun_and_earth.png)

## Initiative

When I was doing a video on about sun and blackb ody radiation lately, I found it particularly hard to plot and visualize data and formulas for blackbody radiation.

Though Planck's Radiation Law is clear on textbook, it's cumbersome in practice to deal with the following aspects: 

1. Handle **input and output units** (say, W/cm2/nm or kW/m2/nm/sr for output units? there're too many different choices for output units)
2. **Irradiance or radiance exitance.** Theoretical formulas talk about radiance exitance, which is the power per area **radiated** by a certain object; But experimental data are mostly irradiance, which is the power **absorbed** per area at a detecter. They need to be carefully handled to compare theoretical and experimental data correctly.

When doing visualizations, I gradually came up with a mini python package that can handle these problems for me. In hope of helping later developers and visualizers on the topic, I decide to make it open source so that they can avoid detours and mistakes.

## Functionality

This repository serves as a basic toolkit for blackbody radiation. The following functionality are provided:

1. Functions for Planck's Law, Wien's Law, Rayleigh-Jeans' Law, with output units and irradiance/radiance exitance properly handled.
2. Wien's displacement Law.
3. Experimental data of solar radiation spectrum(with data loader) for comparison and visualization.(from [https://www.pveducation.org/pvcdrom/appendices/standard-solar-spectra](https://www.pveducation.org/pvcdrom/appendices/standard-solar-spectra))
4. Converters between radiance exitance(of sun) and irradiance(at earth).
5. LaTeX sources for Planck's Law, Wien's Law and Rayleigh-Jeans' Law.

## Setbacks

1. The package was originally designed for science popularization and visualization, so it's NOT tested under extreme data.(milli Kelvin, for example)
2. Not all output units are supported yet. But they can be easily supported by adding convertors, with the rich comments.



## 起因

最近，当我制作有关太阳和黑体辐射的视频时，我发现绘制和可视化黑体辐射的数据和公式特别费劲。虽然普朗克辐射定律在教科书上讲得很清楚，但在实践中以下几个方面处理起来很麻烦：

1. **公式的单位。**（例如，公式单位是 W/cm2/nm 还是 kW/m2/nm/sr？在谱辐射度上，物理单位的选择非常多）
2. **辐照度和辐出率。** 理论公式谈论的是辐出度，它是某个物体单位面积的**向外辐射**功率； 但实验数据往往是辐照度数据，即探测器每个区域**向内吸收**的功率。如果想正确地比较理论和实验数据，就需要进行转换。

在为视频开发可视化效果和动画的过程中，我逐渐积累得到了这个小型的python包。为了帮助其它开发者和可视化工作者，我决定把它开源出来，希望后人可以少走一些弯路，可以在公式单位问题上*少浪费几个周末的下午*。

## 功能

这是一个黑体辐射的基本工具包，提供以下功能：

1. 计算普朗克定律、维恩公式、瑞丽-金斯公式的函数。经过 debug，它们能够正确地处理输出单位和辐照度/辐出度问题。
2. 维恩位移定律。
3. 用于比较和可视化的太阳辐射光谱实验数据（及其加载函数）。（数据来自[https://www.pveducation.org/pvcdrom/appendices/standard-solar-spectra](https://www.pveducation. org/pvcdrom/appendices/standard-solar-spectra))
4. 太阳辐出度和地球所受辐照度之间的转换函数。
5. 普朗克定律、维恩公式和瑞利-金斯公式的 LaTeX 源码。

## 不足

1. 由于一开始是为科普和可视化而开发，因此没有经过极端数据范围的测试。（如毫K级别的温度参数，上百万度的温度参数）
2. 并没有支持所有的公式单位。参照代码中的注释，使用者可以自己添加单位转换函数。