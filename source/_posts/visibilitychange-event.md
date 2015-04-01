title: "关于visibilitychange事件的一点理解"
date: 2015-03-31 13:57:36
tags:
- 技术学习
- javascript
---
## 何为visibilitychange事件
从字面即可很简单的理解到这个事件是在改变可视状态的时候触发，具体来说是在浏览器TAB页切换时触发，经过测试，并不能在最小化浏览器时触发。
> iframe页面可见性与父页面相同，所以通过css显示或隐藏iframe时并不会触发其visibilitychange事件

## 使用方法
```javascript
document.addEventListener("visibilitychange", function() {
    console.log((new Date()));
});
```

## 浏览器兼容性
目前主流的标准浏览器基本都已经支持，部门旧版浏览器需要增加内核前缀，IE从10开始支持。

## 常见应用场景
- 幻灯片播放时可在不可见时停止播放，恢复显示后继续播放
- 每隔一段时间向服务器请求数据的可在切换可见性时停止，减轻服务器负担
- 网站访问统计提供跟准确的数据
- 网站title根据可见性变换

## 参考资料
- https://developer.mozilla.org/en-US/docs/Web/Events/visibilitychange
- https://developer.mozilla.org/en-US/docs/Web/Guide/User_experience/Using_the_Page_Visibility_API
