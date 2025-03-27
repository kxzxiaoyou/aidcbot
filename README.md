# Discord AI Trading Bot 🤖📈

這是一個整合多市場（台股、美股、虛擬貨幣、黃金、商品）並具備 AI 預測能力的 Discord 機器人。
支援按鈕操作介面，功能包含查價、預測、做單信號、自動推播與新聞快報。

---

## ✅ 功能總覽

- 支援多市場（台股、美股、幣圈、黃金、商品）
- Prophet + RSI + LSTM + XGBoost 多模型預測整合
- 圖表產生：價格走勢圖、預測圖、技術指標圖
- 自動做單信號（含信心度判斷）
- Discord 互動式按鈕選單
- 定時任務推播（預測、新聞、波動分析）
- 本機執行 + Render 雲端部署皆可

---

## 🧪 本機使用教學

1. 安裝 Python 3.10+
2. 建立 `.env` 檔，內容如下：

```
DISCORD_TOKEN=你的 Discord Bot Token
```

3. 安裝套件：
```bash
pip install -r requirements.txt
```

4. 啟動機器人：
```bash
python main.py
```

---

## ☁️ Render 雲端部署

1. 到 [https://render.com](https://render.com) 註冊帳號
2. 建立新的 Web Service
3. 上傳此專案並設定：
   - Python 版本：3.10+
   - Start Command：`python main.py`
   - 環境變數加入 `DISCORD_TOKEN`

---

## 📁 檔案說明

| 檔案 | 說明 |
|------|------|
| `main.py` | Discord 主程式與 UI |
| `predictor.py` | 預測模型整合 |
| `market_data.py` | 抓取即時數據 |
| `chart.py` | 圖表產生模組 |
| `scheduler.py` | 定時任務與震盪分析 |
| `news_fetcher.py` | 新聞快報功能 |
| `config.json` | 自訂推播設定 |
| `requirements.txt` | 所需套件列表 |
| `Procfile` | Render 啟動用 |
| `.env.template` | 環境變數格式範例 |

---

