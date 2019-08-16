## iPhoneX 头部适配方案（by qinyf）
使用css适配，属性分为constant（ 兼容 iOS < 11.2）和env（兼容 iOS >= 11.2），都要写。
```
// HTML 代码
<meta name="viewport" content="width=device-width, viewport-fit=cover">

// css 代码
{
  // 兼容 iOS < 11.2
  padding-bottom: constant(safe-area-inset-bottom);
  // 兼容 iOS >= 11.2
  padding-bottom: env(safe-area-inset-bottom);
}

// 使用计算高度
{
  height: calc(60px + constant(safe-area-inset-bottom));
  height: calc(60px + env(safe-area-inset-bottom));
}
```
参考：https://blog.csdn.net/qq_42354773/article/details/81018615
