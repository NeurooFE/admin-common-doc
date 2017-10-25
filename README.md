# 通用管理后台

## 使用

```javascript
import AdminCommon from 'admin-common'

Vue.use(AdminCommon, {store, router, Parse: Vue.prototype.$Parse, config: {title: '测试管理后台'}})

new Vue({
  el: '#app',
  router,
  store,
  template: '<App/>',
  components: { App: AdminCommon.App }
})
```

## 初始化配置

| 属性名    | 描述       | 类型     | 必填    |
| ------ | -------- | ------ | ----- |
| store  | vuex实例   | Object | true  |
| router | router实例 | Object | true  |
| Parse  | Parse实例  | Object | true  |
| config | 通用后台的配置  | Object | false |
| plugin | 通用后台的插件  | Object | false |

### config配置

| 属性名   | 描述          | 类型     | 默认值  | 必填    |
| ----- | ----------- | ------ | ---- | ----- |
| title | 配置头部和登录页的标题 | String | 管理后台 | false |

## 页面配置

通用管理后台分以下几大模块，每个模块都会有对应的配置文档说明：

* [模型属性](模型属性.md)： 定义表中各字段的基础属性，这个模块的配置会影响到 `表格属性` 、`编辑器属性` 和 `查询器属性` 模块。
* [表格属性](表格属性.md)：定义需要在列表中显示的字段和按钮。
* [编辑器属性](编辑器属性.md)：定义需要编辑的字段。
* [查询器属性](查询器属性.md)：定义查询条件。
* [formatter](formatter.md)：定义列表显示时，需要用到的格式化数据的函数体，所定义的函数体在所有列表中都通用。

