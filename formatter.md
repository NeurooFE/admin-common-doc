# formatter

针对是的 `element` 表格的 `formatter` 属性，配置的是一个函数体，函数体的返回值用作表格的显示字段。

定义好 `formatter` 后，在表格属性对应的显示字段配置中将 `formatter` 属性配置为要应用的 `formatter` 名称，在表格渲染时，就会调用对应的函数格式化显示的字段。

注意，不要用高级的语法写 `formatter`，因为此函数体不会参与打包。

函数体的回调参数如下：

| 参数名    | 描述                                       | 类型     |
| ------ | ---------------------------------------- | ------ |
| row    | 当前行对象，跟 `element` 的 `formatter` 的回调参数 `row` 一致。 | Object |
| column | 当前列对象，跟 `element` 的 `formatter` 的回调参数 `column` 一致。 | Object |
| val    | 当前单元格的值                                  | *      |

## example	

```javascript
{
    "date": "return this.dateFormatter(val)",
    "boolean": "return val ? '是': '否'",
    "fenToYuan": "return (val / 100).toFixed(2) + '元'"
}
```

