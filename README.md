# 社交媒体情感分析系统

## 项目概述
基于Hugging Face的DistilBERT模型，对Twitter文本进行情感二分类（正面/负面）。  
在200条测试样本上达到85.5%的准确率。

## 技术细节
- **框架**: Transformers 4.30.2  
- **预训练模型**: [distilbert-base-uncased-finetuned-sst-2-english](https://huggingface.co/distilbert-base-uncased-finetuned-sst-2-english)  
- **训练配置**: 3 epoch, batch_size=16, learning_rate=2e-5

## 结果展示
- 测试集混淆矩阵:  
  ![Confusion Matrix](./confusion_matrix.png)  <!-- 直接引用仓库内图片 -->
  
- 数值明细:  
  |          | 预测负面 | 预测正面 |  
  |----------|---------|---------|  
  | 真实负面 | 73      | 22      |  
  | 真实正面 | 25      | 80      |  

- 关键指标:  
  - 准确率: 76.5% `(73+80)/(73+22+25+80)`  
  - 负面查准率: 74.49% `73/(73+25)`  
  - 正面召回率: 78.43% `80/(22+80)`    
## 在线体验
[Hugging Face Demo](https://huggingface.co/spaces/your-username/sentiment-demo)

## 复现步骤
1. 克隆本仓库
2. 运行 `pip install -r requirements.txt`
3. 执行 `python training_code.ipynb`
