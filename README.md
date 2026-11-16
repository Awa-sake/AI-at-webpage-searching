# AI-at-webpage-searching
An extension composed by DSH for Microsoft Edge as a helper in college learning
中文
1. 我们不收集什么
本扩展没有任何后端服务器、账号体系、统计埋点或崩溃上报。开发者不会收到你的任何数据，也无法知道你在哪些页面使用过它。

2. 数据会去哪里
数据	目的地	触发时机
你选中的文字、页面正文摘录	你自己填写的 API 地址（直连模式），或本机 relay.py → 你自己填写的上游（中继模式）	你点击「一键解题 / 选区 / 本页」时
你框选的页面截图	同上	你点击「截屏」并完成拖框时，或粘贴/拖入图片时
你的 API Key	本机 chrome.storage.local（直连）或本机 relay/config.json（中继）	你保存设置时
面板位置、大小、历史答案缓存	本机 chrome.storage	自动，仅本机
除上述地址外，扩展不会向任何第三方发送数据。 目的地完全由你在设置页填写，开发者无法干预。

3. 本地存储
chrome.storage.sync：中继地址、模型名、截断长度、提示词等设置（若你登录了浏览器账号，会随账号同步）。
chrome.storage.local：面板几何位置、结果缓存（最多 200 条，默认 7 天过期）、直连模式的 API Key。
你可以在配置页「清空缓存」，或在扩展详情页移除扩展，即可清除全部本地数据。
4. 页面访问
扩展会在你访问的网页中注入一个内容脚本，用途仅限于：读取你主动触发时所需的页面文字、显示悬浮窗、在你框选时截取可见区域。脚本不会在后台遍历你的浏览记录，不会读取其他标签页，也不会在未触发时上传任何内容。

5. 第三方模型服务
你填写的 API 提供方会按其自身隐私政策处理这些文本与图片。请自行阅读对应服务的条款；本扩展不代理、不中转、不存储这些内容。

6. 儿童
本扩展不面向 13 岁以下儿童，也不会有意收集其信息（事实上不收集任何人的信息）。

7. 变更与联系
政策变更会随扩展版本更新并在本文件体现。问题请联系：Awasake259@Gmail.com

English
1. What we do not collect
This extension has no backend, no accounts, no analytics and no crash reporting. The developer receives none of your data and cannot tell which pages you used it on.

2. Where data goes
Data	Destination	Trigger
Selected text, page excerpt	The API endpoint you configure (direct mode), or your local relay.py → your configured upstream (relay mode)	When you click Ask / Selection / Page
Screenshot of the region you drag	Same as above	When you finish dragging in Capture mode, or paste/drop an image
Your API key	Local chrome.storage.local (direct) or local relay/config.json (relay)	When you save settings
Panel position/size, cached answers	Local chrome.storage	Automatic, local only
Nothing is sent anywhere else. The destination is entirely user-configured.

3. Local storage
chrome.storage.sync: relay URL, model name, truncation limit, prompt (may sync with your browser account).
chrome.storage.local: panel geometry, answer cache (≤200 entries, 7-day expiry by default), direct-mode API key.
Clear them via "清空缓存" in the options page, or by removing the extension.
4. Page access
A content script is injected so the panel can read the page text you explicitly ask about, render the floating panel, and capture the visible area when you drag a selection box. It does not walk your history, read other tabs, or upload anything without an explicit action.

5. Third-party model providers
Your configured provider processes that text and those images under its own privacy policy. This extension does not proxy, resell or store them.

6. Children
Not directed to children under 13; no personal data is collected from anyone.

7. Changes & contact
Policy changes ship with extension versions and are reflected in this file. Contact: Awasake259@Gmail.com
