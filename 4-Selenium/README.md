# Selenium
[Chrome Options](#Chrome-Options) | [Webdriver 屬性與方法](#webdriver-屬性與方法) | [Webdriver 定位方法](#webdriver-定位方法)

### 安裝套件
```
pip install selenium
```

### 常用的套件
```python
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.common.by import By
```
### Chrome driver download
[Chrome webdriver Link](https://developer.chrome.com/docs/chromedriver/downloads?hl=zh-tw)  

windows 指令下載 (記得修改使用的 Chrome 版本)
```bash
curl -L -o chromedriver.zip "https://storage.googleapis.com/chrome-for-testing-public/<version>/win64/chromedriver-win64.zip"
```

### Chrome Options
| 設定                                       | 說明          |
| ------------------------------------------ | ----------- |
| `add_argument("--headless")`               | 無介面模式       |
| `add_argument("--start-maximized")`        | 最大化視窗       |
| `add_argument(--window-size=1920,1080)`    | 指定視窗大小    |
| `add_argument("--incognito")`              | 無痕模式        |
| `add_argument("--no-sandbox")`             | （Linux 必要）  |
| `add_argument("--disable-popup-blocking")` | 禁止彈跳視窗封鎖    |
| `add_argument("--disable-dev-shm-usage")`  | 避免記憶體共享不足問題 |



### Webdriver 屬性與方法
| webdriver 屬性      | 說明                     |
|---------------------------|--------------------------|
| `current_url`               | 取得目前頁面的 URL       |
| `window_handles`             | 取得所有視窗代號        |
| `title`                     | 取得目前頁面的標題       |
| `page_source`               | 取得完整 HTML 原始碼     |


| webdriver 方法        | 說明                     |
|---------------------------|--------------------------|
| `get(url)`                  | 開啟指定頁面                |
| `refresh()`                    | 刷新頁面 |
| `quit()`                    | 關閉整個瀏覽器與驅動程式 |
| `execute_script(script)`    | 執行 JavaScript 程式碼    |
| `switch_to.window(handle)`   | 切換到指定視窗         |
| `save_screenshot(path)`     | 擷取整頁截圖             |
| `get_cookies()`             | 取得所有 cookie          |
| `add_cookie(cookie_dict)`   | 新增一筆 cookie          |


## Webdriver 定位方法
| 定位方法 | 說明 |
|---|---|
| `find_element(By.ID, 'id')`      | 透過元素的 id 屬性來定位元素。    |
| `find_element(By.NAME, 'name')`      | 透過元素的 name 屬性來定位元素。        |
| `find_element(By.CLASS_NAME, 'class_name')` | 透過元素的 class 屬性來定位元素。       |
| `find_element(By.TAG_NAME, 'tag_name')` | 透過元素的 tag 名稱來定位元素，例如 div, span, a 等。   |
| `find_element(By.LINK_TEXT, 'link_text')`    | 透過完全匹配的超連結來定位 `<a>` 元素。      |
| `find_element(By.PARTIAL_LINK_TEXT, 'partial')` | 透過部分匹配的超連結來定位 `<a>` 元素。    |
| `find_element(By.XPATH, 'xpath')`   | 透過 XPath 表達式來定位元素。適用於複雜的定位需求。     |
| `find_element(By.CSS_SELECTOR, 'selector')`     | 透過 CSS 選擇器來定位元素。   |


