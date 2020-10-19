### 一. 简答题

#### 1. 请简述 Vue 首次渲染的过程。

解题脑图地址：http://naotu.baidu.com/file/7028e70d2d2f31f43f2920a97a19d44a?token=9390504bd09f4504

#### 2. 请简述 Vue 响应式原理。

- 将用户传递过来的 data 中的数据注入到 Vue 实例
- 通过 observe() 将 创建 Observer 实例，并返回
- 在 Observer 中调用 walk() 方法
- 在 walk() 方法中 调用 defineReactive() 方法，将 data 中所有数据转换为响应式数据
- 在转换为响应式数据的同时，在 get 方法中收集依赖，添加到 Dep 的 subs数组中（存储 Watcher对象），在 set 方法中调用 dep 的 notify() 方法通知 Watcher 去更新视图

#### 3. 请简述虚拟 DOM 中 Key 的作用和好处。

- 可以优化渲染过程，减少 Dom 操作，减少 diff 算法的执行时间，提高性能

#### 4. 请简述 Vue 中模板编译的过程。

解题脑图地址：http://naotu.baidu.com/file/ba5f8697cc9441be30e36154db046604?token=0b99965ac5a20cf9

