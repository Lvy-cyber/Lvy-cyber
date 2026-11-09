### 风电 / 气象数据 side projects

用公开再分析资料（ERA5）把风电行业的两条核心链路各跑通一遍：
**规划期的风资源评估**，和**运行期的功率预测**。

| 项目 | 一句话结论 | 技术栈 |
|---|---|---|
| [era5-wind-resource](https://github.com/Lvy-cyber/era5-wind-resource) | ERA5 → 质控 → Weibull → 风切变 → 110 m 外推 → AEP；单机净发电 **11.84 GWh**、容量系数 **27.0%** | Python · pandas · scipy · ERA5 |
| [wind-power-forecast](https://github.com/Lvy-cyber/wind-power-forecast) | 持续法 / 气候态 / Ridge / GBDT × 1–24 h；24 h 准确率 **67.5%**（较持续法降误差 21.4%） | Python · scikit-learn |

两个项目共用同一站址（内蒙古辉腾锡勒，41.25°N / 112.75°E）与同一机型口径，结论可对照：
前者回答"这地方一年能发多少电"，后者回答"明天这个时候能发多少"。

两个仓库都带完整报告（6–7 页 PDF）、全部图表与一键复现脚本。

> 数据：ERA5（Copernicus Climate Change Service / ECMWF，CC BY 4.0），经 Open-Meteo 获取。
> 两个项目均为方法复现，不构成工程咨询或发电计划建议。
