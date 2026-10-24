# DeepAnalyze

**简体中文** | [English](README.md)

面向自动化数据科学的 DeepAnalyze 上游项目 fork，包含模型推理代码、数据分析示例、Web 演示和 Docker 环境。本说明为中文使用入口，上游英文论文介绍、引用与作者信息继续保留。

## 环境要求

适合 vLLM / PyTorch 的 Linux、CUDA 与 NVIDIA GPU 环境；模型权重需另外下载。具体依赖见 requirements.txt，显存需求由模型和推理设置决定。

## 获取仓库

```bash
git clone https://github.com/RoxyXu151/DeepAnalyze.git
cd DeepAnalyze
```

私有仓库需要先通过 GitHub 认证。以下相对路径与操作均以本仓库为起点。

## 安装与启动

```bash
python -m pip install -r requirements.txt
```

## 配置与准备

run.py 中的模型路径和 workspace 是上游开发环境路径，运行前必须替换成本机已准备的模型和输入目录。使用 Docker 时先阅读 docker/README.md，Compose 默认启动 shell，不会自动启动模型 API。

## 使用方法与产物

准备可信的数据工作区，按英文 README 的 DeepAnalyzeVLLM 示例调用模型。run.py 展示 prompt、workspace 与 generate 的调用；输出包括推理文本和工作区产物。Web 演示入口在 demo/，独立服务需按其脚本配置。

## 仓库导览

- [requirements.txt](requirements.txt)
- [run.py](run.py)
- [demo](demo)
- [docker](docker)
- [example](example)
- [CONTRIBUTION.md](CONTRIBUTION.md)
- [docker/README.md](docker/README.md)
- [example/README.md](example/README.md)

## 验证与常见问题

用小型数据和简单问题检查模型加载、文件读取与产物。生成代码和分析需人工核验；当前文档更新未运行 GPU 推理或复现论文指标。贡献说明与 citation 继续见英文主页和 CONTRIBUTION.md。

## 维护与贡献

修改功能或使用方式时同步更新中英文 README。问题反馈请附复现步骤、环境版本与去除敏感信息后的日志；提交改动时说明实际完成的验证。

## 许可与来源

许可条款以仓库的 [LICENSE](LICENSE) 为准。第三方代码、数据、模型、论文与素材保留各自的许可和署名。

本仓库为 fork，原有上游作者、引用和版权说明继续保留。
