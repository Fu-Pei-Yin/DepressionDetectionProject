# Depression Detection via Multimodal AI

## 📘 專題簡介
本專題旨在透過多模態生成式 AI，整合文字、語音與視覺數據，建構一套可預測社群使用者憂鬱傾向的模型架構。
使用 LLM 生成模擬貼文資料，以解決真實資料稀缺與隱私限制問題，提升模型準確度與泛化能力。

## 📂 專案結構

DepressionDetectionProject/
├── notebooks/ # 主要 Colab Notebook 程式
├── data/ # 放置資料集（可用假資料作測試）
├── features/ # 儲存模型中介特徵
├── models/ # 模型儲存位置
├── scripts/ # OpenFace 或自動化腳本
├── .github/workflows/ # GitHub Actions 自動部署設定
├── README.md # 說明文件

markdown
複製
編輯

## 🚀 一鍵開啟 Colab

| Notebook 說明 | 開啟連結 |
|---------------|-----------|
| 預處理與資料切分 | [Open in Colab](https://colab.research.google.com/github/Fu-Pei-Yin/DepressionDetectionProject/blob/main/notebooks/01_data_preprocessing.ipynb) |
| 特徵提取 | [Open in Colab](https://colab.research.google.com/github/Fu-Pei-Yin/DepressionDetectionProject/blob/main/notebooks/02_feature_extraction.ipynb) |
| 模型訓練 | [Open in Colab](https://colab.research.google.com/github/Fu-Pei-Yin/DepressionDetectionProject/blob/main/notebooks/03_model_training.ipynb) |
| 評估與視覺化 | [Open in Colab](https://colab.research.google.com/github/Fu-Pei-Yin/DepressionDetectionProject/blob/main/notebooks/04_evaluation.ipynb) |
| 虛擬貼文生成 | [Open in Colab](https://colab.research.google.com/github/Fu-Pei-Yin/DepressionDetectionProject/blob/main/notebooks/05_generate_virtual_text.ipynb) |

## 📊 甘特圖（進度規劃）

![Gantt Chart](gantt_chart.png)

## 📁 假資料說明

請將資料放在 `data/` 資料夾中，建議結構如下：

data/
├── sample_dialogue.json # 模擬訪談內容（文字）
├── sample_audio.wav # 模擬音訊（語音）
├── sample_openface.csv # 模擬 OpenFace 特徵（臉部）

shell
複製
編輯

## 🔧 執行需求

```bash
pip install -r requirements.txt
# 或手動安裝：
pip install torch transformers librosa scikit-learn pandas
🔐 OpenAI API Key
若使用 05_generate_virtual_text.ipynb 生成貼文，請至程式中填入你的 OpenAI API 金鑰：

python
複製
編輯
import openai
openai.api_key = "your-key-here"
