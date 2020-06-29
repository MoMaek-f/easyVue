# vue固钉/vue-affix/vue图钉

固钉组件, 可以将内容固定在屏幕上，并且不随页面的滚动而滚动，常用于侧边菜单和导航栏等

在vue的项目中经常用到固钉，但是 [element-ui](http://element-cn.eleme.io/#/zh-CN/component/installation) 上并没有提供这样的组件可供使用，[ant-design-vue](https://vuecomponent.github.io/ant-design-vue/components/affix-cn/) 有提供，总不能为了这一个组件再去引入一个组件库吧

这是一个封装好的 affix 组件，可以放到项目中直接使用

> 将Affix.vue文件添加至项目组件，然后按照下面的用法即可

# useage：

```vue
<template>
    <div class="test">
        <my-affix>
            <div>这是一个固钉组件</div>
        </my-affix>
        <my-affix :offset="40">
            <div>这是一个固钉组件</div>
        </my-affix>
    </div>
</template>

<script>
import Affix from '@/components/Affix';
export default {
    name: 'test',
    components: {
        "my-affix" : Affix
    }
};
</script>
```

| 参数     | 说明                                                         | 类型              | 默认值 |
| -------- | ------------------------------------------------------------ | ----------------- | ------ |
| offset   | 距离窗口顶部达到指定偏移量后触发                             | Number            | 0      |
| boundary | 设置 Affix 的活动范围，值为affix上级元素的id(可以是父元素，也可以是父元素的父元素...) | String(#parent)   |        |
| on-affix | 固定状态改变时触发的回调函数                                 | Function(affixed) | 无     |