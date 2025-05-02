# MiBandGMaps 導航應用

![image](https://github.com/andyching168/MiBandGMaps/blob/main/xiaomi_band-2025-05-02-23-52-05.png)

這是一個用於小米手環的 Google Maps 導航應用，可以將手機上的導航信息同步到手環上顯示。
需搭配[Android端APP](https://github.com/andyching168/MiBandGMaps-Android)使用
## 功能特點

- 實時顯示導航方向（左轉、右轉、直行等）
- 顯示當前道路名稱
- 顯示到下一個轉彎點的距離
- 自動調整屏幕亮度
- 支持演示模式（用於開發調試）

## 開發說明

### 演示模式

在開發過程中，可以使用演示模式來測試 UI 效果：

1. 在 `src/pages/index/index.ux` 中設置：
   ```javascript
   private: {
     isDemoMode: true,  // 設置為 true 啟用演示模式
     // ... 其他配置
   }
   ```

2. 演示模式會自動循環顯示預設的導航信息，每 5 秒切換一次。

### 部署注意事項

在部署到實際設備前，請確保：

1. 關閉演示模式：
   ```javascript
   private: {
     isDemoMode: false,  // 設置為 false 禁用演示模式
     // ... 其他配置
   }
   ```

2. 確保 `isSimulator` 設置為 `false`：
   ```javascript
   private: {
     isSimulator: false,  // 設置為 false 以使用實際設備功能
     // ... 其他配置
   }
   ```

## 技術要求

- 小米手環（支持互聯功能的型號）
- 手機端需要安裝配套的 Google Maps 導航應用
- 需要開啟藍牙連接

## 開發環境

- 使用快應用開發工具
- 支持模擬器調試
- 支持真機調試

## 注意事項

1. 在模擬器中運行時，某些功能（如亮度控制）可能無法正常工作
2. 實際部署時請確保關閉演示模式
3. 確保手機和手環之間的藍牙連接穩定
