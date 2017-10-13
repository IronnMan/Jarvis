# 用 JavaScript 检测浏览器在线／离线状态（JavaScript API——navigator.onLine）

如今 HTML5 移动应用或 Web app 中越来越普遍的使用了离线浏览技术，所以 JavaScript 检测浏览器在线／离线状态非常常见。无论浏览器是否在线，`navigator.onLine` 属性都会提供一个布尔值。如果浏览器在线，则设置为 `true`，否则设置为 `false`。

```javascript
if(navigator.onLine) { // true|false

}
```

## online 和 offline 事件

当浏览器脱机或上线时，浏览器还支持 `online` 和 `offline` 事件。

```javascript
window.addEventListener('online', function(e){console.log('online')});
window.addEventListener('offline', function(e){console.log('offline')});
```
你可以使用几种熟悉的方式来注册事件：
+ 在 `window`，`document`，或 `document.body` 上使用 `addEventListener`
+ 将 `document` 或 `document.body` 的 `ononline` 或 `onoffline` 属性设置为一个 JavaScript Function 对象。（注意：由于兼容性原因，不能使用 `window.ononline` 或 `window.onoffline`。）
+ 在 HTML 标记中的 `body` 标签上指定 ononline="..." 或 onoffline="..." 特性。


## 注意事项

+ IE8 中需要给 document.body 绑定事件而不是 window
+ 在线离线的变化指的是物理上的网络链接变化，如果是在控制台将网络限制为 offline 则不会触发相应的事件。
+ 兼容性
    + IE: 8+
    + Chrome: 14+
    + Firefox: 3.5+
    +