# supply-chain-demand-forecasting
供应链需求预测项目
# 供应链需求预测 Demo

基于公开 Superstore 零售数据集的需求预测与安全库存测算小项目。

## 背景与目标
针对"需求预测 + 库存控制"进行实操练习，输出可复用的
"需求预测 → 补货参数计算"流程。

## 数据
Sample-Superstore（2014–2017 订单明细），按周聚合销售额作为需求口径。

## 方法
- 移动平均 / 加权移动平均 / 简单指数平滑 / Holt 趋势 / Holt-Winters
- 评估指标：MAE / RMSE / MAPE，择优
- 安全库存 SS = Z·σ·√L，再订货点 ROP，经济订货批量 EOQ

## 结果
- 最优模型：Holt-Winters，测试集 MAPE = 50.48%
- 输出子品类级安全库存 / ROP / EOQ 参数表

## 运行
pip install -r requirements.txt
python demand_forecast.py

