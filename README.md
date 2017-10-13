# 用 JavaScript 检测浏览器在线／离线状态（JavaScript API——navigator.onLine）

如今 HTML5 移动应用或 Web app 中越来越普遍的使用了离线浏览技术，所以 JavaScript 检测浏览器在线／离线状态非常常见。无论浏览器是否在线，`navigator.onLine` 属性都会提供一个布尔值。如果浏览器在线，则设置为 `true`，否则设置为 `false`。

```javascript
if(navigator.onLine) { // true|false

}
```