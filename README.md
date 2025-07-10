# 眼部健康大模型项目

## 项目简介
本项目是一个集成多种眼部健康相关功能的智能系统，支持症状咨询、图片识别、视力检测、用户记忆管理、知识库查询等。系统包含命令行和Web前端，适合科研、医疗辅助等场景。

## 主要功能
- **症状智能问诊**：通过大模型API分析用户输入的症状，给出诊断建议。
- **眼部图片识别**：上传眼部图片，自动识别常见眼病（如白内障、青光眼等）。
- **视力检测**：基于摄像头和手势识别的E字视力表测试。
- **用户记忆管理**：记录用户历史咨询、检测结果，实现个性化服务。
- **知识库查询**：内置常见眼病知识库，支持症状与疾病的智能匹配。
- **Web前端**：提供简洁的网页交互界面。

## 文件结构与说明
- `main.py`：命令行主程序，集成症状问诊、图片分析、视力检测等功能。
- `app.py`：Flask Web服务主程序，提供API和网页前端。
- `api_integration.py`：大模型API（如DeepSeek）集成与调用。
- `image_processing.py`：眼部图片识别与模型推理。
- `vision_test.py`：摄像头E字视力检测与手势识别。
- `train_model.py`：眼病识别模型的训练脚本。
- `memory_manager.py`：用户记忆的读写管理。
- `ocular_disease_knowledge_base.py`：常见眼病知识库及症状匹配。
- `test_api.py`：API接口测试脚本。
- `user_memory.json`：用户历史数据存储。
- `best_model.pth`/`full_model.pth`：训练好的模型权重文件。
- `templates/`：前端网页模板（如index.html）。
- `pictures/`：E字图片等素材。

## 依赖环境
请先安装Python 3.8及以上版本。

安装依赖：
```bash
pip install -r requirements.txt
```

## 运行方式
### 命令行交互
```bash
python main.py
```

### 启动Web服务
```bash
python app.py
```
访问 http://localhost:5000 即可使用网页前端。

## 说明
- 训练模型需准备好数据集并修改`train_model.py`中的路径。
- 视力检测需电脑有摄像头。
- 各模块均有测试代码，可单独运行。

## 致谢
本项目参考了多种开源实现，感谢相关社区的支持。

