# 前后端交互案例


## 启动

```sh
node server.js 8888
```

## 功能概述

使用 nodejs 做后台判断，每次加载页面(`./`)请求 db 文件的数据，当点击 付款 的 input 按钮时，发送一个地址为`/pay` 的 `POST` 请求，nodejs 后台判断请求为 `/pay` 并且为 `POST` 请求时修改 `db` 文件，将db文件中的数字减一

## iframe标签

作用：在页面中添加一个 iframe 标签，用来承载 form 表单提交后展示的结果 在 target 的中添加 iframe 中 name 对应的属性

```html
<form action="/pay" method="POST" target="result">
    <input type="submit" value="付款">
</form>
<iframe name="result" src="about:blank" frameborder="0" height="100"></iframe>
```

