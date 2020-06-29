在vue的项目中经常用到固钉，但是 [element-ui](http://element-cn.eleme.io/#/zh-CN/component/installation) 上并没有提供这样的组件可供使用，[ant-design-vue](https://vuecomponent.github.io/ant-design-vue/components/affix-cn/) 有提供，总不能为了这一个组件再去引入一个组件库吧

下面是一个封装好的 affix 组件，可以放到项目中直接使用

# useage：

```vue
<template>
    <div class="test">
        <affix>
            <div>这是一个固钉组件</div>
        </affix>
        <affix :offset="40">
            <div>这是一个固钉组件</div>
        </affix>
    </div>
</template>

<script>
import Affix from '@/components/Affix';
export default {
    name: 'test',
    components: {
        Affix
    }
};
</script>
```

| 参数     | 说明                                                         | 类型              | 默认值 |
| -------- | ------------------------------------------------------------ | ----------------- | ------ |
| offset   | 距离窗口顶部达到指定偏移量后触发                             | Number            | 0      |
| boundary | 设置 Affix 的活动范围，值为affix上级元素的id(可以是父元素，也可以是父元素的父元素...) | String(#parent)   |        |
| on-affix | 固定状态改变时触发的回调函数                                 | Function(affixed) | 无     |