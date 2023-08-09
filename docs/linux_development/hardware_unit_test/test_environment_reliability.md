---
sidebar_position: 1
---

# 环境可靠性测试（定频）

## 测试方法

1.	进入到`test_tools/01_cpu_bpu_ddr`文件夹下，执行`sh cpubpu.sh &`脚本，对`bpu`，`cpu`进行压力测试，当前配置启动双`bpu`运行到最高99%负载，`cpu` 90%以上负载，内存随机读写
2.	可以在脚本中更改运行时间及负载强度
3.	打开终端记录运行log

## 测试标准

1. 高温：45°、低温：-10°、常温下，程序正常执行，不会出现重启挂死的情况。
2. LOG中没有`fail`、`error`、`timeout`等异常打印。
3. 能稳定运行48小时。
4. 运行过程中需要关注CPU、BPU占比，使CPU占比均接近90%，BPU压力接近90%。