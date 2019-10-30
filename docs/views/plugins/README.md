---
title: Introduce
date: 2019-09-30
---

:::tip
主题从 `vuepress-theme-reco@1.1.0` 版本之后，开始进行插件化，将能够独立的功能或组件封装成插件，精简核心代码，方便维护和扩展。
:::

## 插件是什么

### 插件分两种：
- **`vuepress-theme-reco` 独占**：因为和主题存在某种耦合，仅适合本主题使用；
- **`vuepress` 主题公用**：可以在所有 `vuepress` 主题使用。

## 插件怎么用

### 使用插件

在下载插件后，你可以通过在 `.vuepress/config.js` 中做一些配置来使用插件
```javascript
module.exports = {
  plugins: [ 'vuepress-plugin-xx' ]
}
```

### 配置插件的选项

#### Babel式

```javascript
module.exports = {
  plugins: [
    [
      'vuepress-plugin-xxx',
      { /* options */ }
    ]
  ]
}
```

#### 对象式

```javascript
module.exports = {
  plugins: {
    'xxx': { /* options */ }
  }
}
```

### 禁用插件

#### Babel式

```javascript
module.exports = {
  plugins: [
    [ 'xxx', false ] // disabled.
  ]
}
```

#### 对象式

```javascript
module.exports = {
  plugins: {
    'xxx': false // disabled.
  }
}
```

[关于插件的使用的详细文档](https://vuepress.vuejs.org/zh/plugin/using-a-plugin.html#%E4%BD%BF%E7%94%A8%E6%8F%92%E4%BB%B6)