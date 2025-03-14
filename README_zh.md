# BeeSeeR
這是一個螢幕 OCR 工具，用類似螢幕截圖的方法解析文字。

## 概述
BeeSeeR是一個方便使用的螢幕光學字符識別（OCR）工具，設計成可以快速地從螢幕上的任何區域提取文字訊息至剪貼簿中。

⚠ **重要提醒:** 這個腳本因為用到選擇電腦桌面特定區域等等的自動化功能，我不確定會不會觸發防外掛程式，如果要在線上遊戲中(特別是競技遊戲)使用要自行承擔後果喔！

## 應用
https://github.com/user-attachments/assets/340bdbb9-ad20-4f22-bf8c-2db590b9c0d9

- **從螢幕擷取文字供 LLM（大語言模型）使用**（如 ChatGPT、Claude），避免輸入限制，同時滿足多語言互相翻譯。
- **直接從 PC 遊戲畫面擷取文字**。

## 功能特色
- **一鍵提取文字** – 無需手動儲存截圖。
- **直覺式操作介面** - 快速擷取並識別文字。
- **剪貼簿整合** – 文字自動複製，方便貼上。
- **支援多種語言** – 以 `Surya模型` 為基礎，可適應90+種語言。
- **最佳化速度** – 可選擇啟用 GPU 加速，以提升處理效率。

## 系統需求
- **Windows 10/11**
- **Python 3.10 - 3.13**
- **NVIDIA GPU（建議）** – 使用 CUDA 加速提高 OCR 速度。

## 下載
- 複製存儲庫到電腦
   ```bash
   git clone https://github.com/KuoCT/BeeSeeR.git
   cd BeeSeeR
   ```

## 安裝
### 使用 NVIDIA GPU 加速的 `兼容模式` (推薦使用)
- 執行 `BeeSeeR.bat` 進行首次安裝。
- 首次安裝完成後，使用者可以自由切換成 CPU 模式，只要編輯`BeeSeeR.bat` 設定 `mode` 成 `1`:
   ```bat
   :: 設定模式（0 為兼容模式，1 為強制CPU模式）
   set mode=1
   ```
- 設定 `debug` 成 `0` 可以隱藏 terminal 視窗(確定可以正常運行後使用):
   ```bat
   :: 設定 debug 變數（0 為背景執行模式，1 為除錯模式）
   set debug=0
   ```
- 存檔 `BeeSeeR.bat` 供後續使用。

### 使用 `強制 CPU 模式` (占用空間較小，處理速度較慢，適合沒有 NVIDIA GPU 的使用者)
- 編輯 `BeeSeeR.bat` 設定 `mode` 成 `1`，然後不要更改它。
- 執行 `BeeSeeR.bat` 進行首次安裝。
- 首次安裝完成後，在 `BeeSeeR.bat` 中設定 `debug` 成 `0` 可以隱藏 terminal 視窗(確定可以正常運行後使用)
- 存檔 `BeeSeeR.bat` 供後續使用。

首次運行可能需要一些時間，因為會自動安裝所需的依賴項。**請等到OCR小視窗彈出表示安裝完成。**

🛠 **工具:** `fix.bat` 可以幫你解除安裝 pytorch 相關的套件，當你需要修改初始安裝成 `兼容模式` 或是 `強制 CPU 模式` 時使用。

## 使用方式
1. 啟動 BeeSeeR – 執行 `BeeSeeR.bat`。
2. 點擊 `Caprure` 按鈕 – 選擇螢幕上的任何區域。
3. 文字將被即時提取且自動複製到剪貼簿 – 可直接貼上到任何地方 (例如 ChatGPT)。
4. 在資料夾中可以找到並編輯 `User_prompt.txt` 中的文字，它會作為提示詞一起被複製到剪貼簿！(不想要複製提示詞的話取消勾選提示詞的核取方塊即可)

## 致謝
特別感謝以下開源專案的支持：
- [Surya](https://github.com/VikParuchuri/surya) – 由 VikParuchuri 開發的強大 OCR 模型。
- [PyAutoGUI](https://github.com/asweigart/pyautogui) – 由 asweigart 開發的直觀自動化工具。
- [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) – 由 TomSchimansky 開發的美觀現代 UI 庫。
