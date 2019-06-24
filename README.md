# v-skeleton
一个简易的骨架屏 基于element-ui的栅格布局 (后面就不用啦！

![skeleton](https://i.loli.net/2019/06/24/5d106994017b260227.gif)

# 安装
```javascript
npm i v-skeleton

yarn add v-skeleton
```
# 使用

```javascript
<template>
  <div v-skeleton="showSkeleton">
    <!-- something -->
  </div>
</template>

<script>
import Vue from 'vue'
import Skeleton from 'v-skeleton'

Vue.use(Skeleton)

  export default {
    data() {
      return {
        showSkeleton: true
      }
    }
  }
</script>
```


> 在nuxt中挣扎了半天 最后写了这个临时使用
