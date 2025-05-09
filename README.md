# Comfyui-Memory_Cleanup

Comfyui-Memory_Cleanup 是一个用于 ComfyUI 的自定义节点，提供内存清理功能以优化 ComfyUI 的运行性能。

## 功能介绍

![使用示例1](1.png)

![使用示例2](2.png)

### 主要功能

本插件提供两个主要节点：

#### 1. 🎈VRAM-Cleanup (GPU显存清理)

可以帮助释放 GPU 显存，主要功能：
- 卸载模型 (offload_model)
- 清理显存缓存 (offload_cache)

#### 2. 🎈RAM-Cleanup (系统内存清理)

可以帮助释放系统内存，支持 Windows 和 Linux 系统：
- 清理文件缓存 (clean_file_cache)
- 清理进程内存 (clean_processes)
- 清理未使用的 DLL (clean_dlls)
- 支持多次重试 (retry_times)


## 安装方法

1. 将此仓库克隆或下载到您的 ComfyUI 自定义节点目录：
   ```
   git clone https://github.com/LAOGOU-666/Comfyui-Memory_Cleanup.git
   ```
   或直接下载 ZIP 解压到 `custom_nodes` 目录

2. 安装依赖：
   ```
   pip install -r requirements.txt
   ```

3. 重启 ComfyUI

## 使用方法

1. 在节点浏览器中搜索 "Memory Management" 分类
2. 将 🎈VRAM-Cleanup 或 🎈RAM-Cleanup 添加到您的工作流中
3. 连接到工作流的适当位置，通常放在生成完成后

## 参数说明

### VRAM-Cleanup
- anything: 可以连接任何输入
- offload_model: 是否卸载模型
- offload_cache: 是否清理显存缓存

### RAM-Cleanup
- anything: 可以连接任何输入
- clean_file_cache: 是否清理文件缓存
- clean_processes: 是否清理进程内存
- clean_dlls: 是否清理未使用DLL
- retry_times: 重试次数 (1-10)

## 注意事项

- 内存清理可能会导致性能暂时下降，但可以防止长时间运行时的内存泄漏
- 建议在重要节点完成工作后使用此节点


# 如果您受益于本项目，不妨请作者喝杯咖啡，您的支持是我最大的动力

<div style="display: flex; justify-content: left; gap: 20px;">
    <img src="https://raw.githubusercontent.com/LAOGOU-666/Comfyui-Transform/9ac1266765b53fb1d666f9c8a1d61212f2603a92/assets/alipay.jpg" width="300" alt="支付宝收款码">
    <img src="https://raw.githubusercontent.com/LAOGOU-666/Comfyui-Transform/9ac1266765b53fb1d666f9c8a1d61212f2603a92/assets/wechat.jpg" width="300" alt="微信收款码">
</div>

# 商务合作
如果您有定制工作流/节点的需求，或者想要学习插件制作的相关课程，请联系我
wechat:wenrulaogou2033