# 建立伺服器

您的 Client ID 和 Secret 應受到保護並保持其機密性，因您的所有檔案都與您的開發者帳號繫結在一起，所以在進行網頁應用程式開發時，請確保 Client ID 和 Secret 只存在於您的伺服器上，並未對外曝露。本章節將示範如何建立本地開發用途的伺服器。

有關必要的軟體，請檢閱[「開發工具及環境準備」](/zh-TW/environment/tools/)章節。

### 事前准备

**ngrok**

當 Design Automation 修改完模型後，將會發出通知。由於您的電腦未公開到網路上，[ngrok](https://ngrok.com/) 工具會建立一個暫存位址以接收通知。此工具僅在本端需要。 

下載後，請將其解壓縮。開啟 Windows **指令行提示** (CMD) 並導覽至該資料夾。然後執行 `ngrok http 3000 -host-header="localhost:3000"`。複製**轉送** URL 值 (採用 `http://1ab2c3d4.ngrok.com` 形式)

![](/_media/designautomation/ngrok.gif)

> 如果在非 Windows (例如 MacOS) 上執行，請改為開啟 **Terminal** 並遵循相同的步驟，但需要以 `./` 為前綴。

!> **警告**：`ngrok` 會在您的 localhost 伺服器使用時將其公開到網路。請務必在測試完成後將其關閉。請勿在開發環境以外使用此工具

設定專案，然後選擇您的語言：[Node.js](/zh-TW/environment/setup/nodejs_da) | [.NET Core](/zh-TW/environment/setup/netcore_da)