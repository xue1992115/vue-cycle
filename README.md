# vue-sycle

> vue 生命周期

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

## vue 生命周期

- `beforeCreate`
  实例创建前，这个阶段实例的 data、methods 是读不到的.
- `created`
  实例创建后：这个阶段已经完成了数据观测(data observer)，属性和方法的运算， watch/event 事件回调。mount 挂载阶段还没开始，$el 属性目前不可见，数据并没有在 DOM 元素上进行渲染。
- `beforeMount`
  在挂载开始之前被调用：相关的 render 函数首次被调用。
- `mounted`
  el 选项的 DOM 节点 被新创建的 vm.$el 替换，并挂载到实例上去之后调用此生命周期函数。此时实例的数据在 DOM 节点上进行渲染
- `beforeUpdate`
  数据更新时调用，但不进行 DOM 重新渲染，在数据更新时 DOM 没渲染前可以在这个生命函数里进行状态处理
- `updated`
  这个状态下数据更新并且 DOM 重新渲染，当这个生命周期函数被调用时，组件 DOM 已经更新，所以你现在可以执行依赖于 DOM 的操作。当实例每次进行数据更新时 updated 都会执行
- `beforeDestory`
  实例销毁之前调用。
- `destroyed`
  Vue 实例销毁后调用。调用后，Vue 实例指示的所有东西都会解绑定，所有的事件监听器会被移除，所有的子实例也会被销毁。

## vue 生命周期在真实场景下的应用

- `created`：进行 ajax 请求异步数据的获取、初始化数据
- `mounted`：挂载元素内 dom 节点的获取
- `nextTick`：针对单一事件更新数据后立即操作 dom
- `updated`：任何数据的更新，如果要做统一的业务逻辑处理
- `watch`：监听具体数据变化，并做相应的处理、

## 生命周期图

![image](https://github.com/xue1992115/vue-cycle/raw/master/assets/cycle.png)

https://github.com/用户名/repository仓库名/raw/分支名master/图片文件夹名称/***.png
