# 基於 RAG 的聊天機器人

這是一個基於檢索增強生成 (Retrieval-Augmented Generation, RAG) 的聊天機器人，使用 Wikipedia 作為知識檢索來源，並結合 Ollama 提供的語言模型生成答案。

---

## 功能簡介

- **檢索模組**：透過 Wikipedia API 從中文維基百科中檢索相關的背景知識。
- **生成模組**：結合檢索結果，使用語言模型生成智慧化的回答。
- **互動模式**：支持用戶與機器人進行自然語言交互。

---

## 安裝與執行

### 環境準備
請確保您的系統已安裝 Python 3.7 或更高版本，並安裝以下依賴：
1. [wikipedia-api](https://pypi.org/project/wikipedia-api/) 用於檢索 Wikipedia 條目。
2. [requests](https://pypi.org/project/requests/) 用於與 Ollama API 進行通信。

### 安裝步驟
1. **克隆存儲庫**
   ```bash
   git clone https://github.com/your-username/rag-chatbot.git
   cd rag-chatbot
2. **建立虛擬環境並安裝依賴**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # 對於 Windows 系統： .\\.venv\\Scripts\\activate
   pip install -r requirements.txt

3. **創建 requirements.txt 文件**（如果尚未存在） 在項目目錄下，創建 requirements.txt 文件，內容如下：
   ```bash
   wikipedia-api
   requests
### 使用說明
1. **運行聊天機器人** 運行以下命令啟動機器人：
   ```bash
   python RAG_llama3.py

2. **交互操作** 啟動後，輸入您的問題。機器人會檢索相關資料，並生成答案。例如：
   ```bash
   你：台北101的高度是多少？
   機器人：台北101的高度為 508 公尺，是曾經的世界第一高樓。

3. **結束聊天**
   ```bash
   輸入 exit 或 quit 即可結束程序。

---

### 注意事項
1. **User-Agent 設置** 請在程式碼中的 user_agent 字段填入專案的實際資料。例如：
   ```bash
   user_agent = 'rag-chatbot/1.0 (https://github.com/your-username/rag-chatbot; email@example.com)'
2. **API Token** 如果您使用的是私有模型或需要特定的 API Token，請確保正確配置 API。
3. **Wikipedia** 使用規範 請務必遵守 Wikipedia 的 User-Agent 政策。




