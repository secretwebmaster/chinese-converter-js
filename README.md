# Chinese Converter JS
Chinese-Converter.js 用於在網頁上實現繁體中文與簡體中文的即時轉換，不會改變原始 HTML 結構。

## 功能特點

- 支持繁體中文與簡體中文之間的相互轉換。
- 即時翻譯網頁內容，無需重新加載頁面。
- 保存用戶語言偏好，通過 Cookie 實現語言設置持久化。
- 易於集成，通過簡單的配置即可使用。

## 文件名

`chinese-converter.js`

## 使用方法

### 1. 引入 JavaScript 文件

將 `chinese-converter.js` 文件添加到您的項目中，並在 HTML 頁面中引入：

```html
<script src="chinese-converter.js"></script>
```

### 2. 添加翻譯按鈕

在您的 HTML 中添加一個按鈕用於切換語言，並設置按鈕的 `id` 為 `translateLink`（默認值）：

```html
<button id="translateLink">繁體</button>
```

### 3. 初始化翻譯功能

在頁面加載完成後，初始化翻譯功能：

```html
<script>
    // 初始化 Chinese-Converter.js
    document.addEventListener('DOMContentLoaded', function () {
        initializeTranslation();
    });
</script>
```

### 4. 自訂配置（可選）

若需要更改默認設置，例如按鈕文本或默認語言，可以直接修改以下變數：

```javascript
var defaultEncoding = 2; // 默認語言：1-繁體中文，2-簡體中文
var msgToTraditionalChinese = "切換至繁體";
var msgToSimplifiedChinese = "切換至簡體";
var translateButtonId = "customTranslateLink"; // 自訂按鈕 ID
```

### 5. 完整範例

以下是一個完整的 HTML 示例，展示如何使用該庫：

```html
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chinese-Converter.js Demo</title>
    <script src="chinese-converter.js"></script>
</head>
<body>
    <h1>歡迎使用 Chinese-Converter.js</h1>
    <p>這是一個示例文本，用於測試繁簡中文的即時轉換。</p>
    <button id="translateLink">繁體</button>
    
    <script>
        document.addEventListener('DOMContentLoaded', function () {
            initializeTranslation();
        });
    </script>
</body>
</html>
```

## 注意事項

1. 確保您的按鈕 ID 與腳本中的配置匹配。
2. 該腳本使用 Cookie 保存用戶的語言偏好，因此需要啟用瀏覽器的 Cookie 功能。
3. 建議在網頁加載後調用 `initializeTranslation()` 方法，確保正確設置語言狀態。

## 授權

此項目基於 MIT 許可證發布，歡迎自由使用與修改。
