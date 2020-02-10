<p align="center">
  <img src="./public/mindmap.png" width="300"/>
</p>

# 思维导图组件-mindmap

功能：拖拽、编辑、删除、添加、缩放...

支持键盘和鼠标操作

- Tab - 添加子节点
- Enter - 添加兄弟节点
- delete - 删除节点
- 右键 - 菜单
- 单击两次 - 编辑
- ...

在线演示：<https://mindnode.5xin.xyz>

## 背景-Background

初衷是想实现一个跟[MindNode](https://mindnode.com)近似的网页思维导图web mindmap

目前正尝试将思维导图组件化

目标是实现一个完整的思维导图组件

## 安装-Install

```sh
npm install @hellowuxin/mindmap
```

```js
// 在你的vue文件中引入思维导图组件
import mindmap from '@hellowuxin/mindmap'
```

## 使用方法-Usage

| Name    | Type   | Default   | Description    |
| ---     | ---    | ---       | ---            |
| v-model | Array  | undefined | 设置思维导图数据  |
| width   | Number | 700       | 设置组件宽度     |
| height  | Number | 700       | 设置组件高度     |

## 样例-Example

```html
<template>
  <div id="app">
    <mindmap
      v-model="data"
    ></mindmap>
  </div>
</template>

<script>
import mindmap from '@hellowuxin/mindmap'

export default {
  name: 'App',
  components: {
    mindmap
  },
  data: () => ({
    data: [{
      "name":"如何学习D3",
      "children":
      [
        {
          "name":"预备知识",
          "children":
          [
            {"name":"HTML & CSS", "children": []},
            {"name":"JavaScript", "children": []}
        },
        {
          "name":"安装",
          "children": []
        },
        ...
      ]
    }]
  })
}
</script>
```
