---
type: Feedback
category: Components
subtitle: 对话框
title: Modal
---

模态对话框。

## 何时使用

需要用户处理事务，又不希望跳转页面以致打断工作流程时，可以使用 `Modal` 在当前页面正中打开一个浮层，承载相应的操作。

另外当需要一个简洁的确认框询问用户时，可以使用精心封装好的 `Vue.$modal.confirm()` 等方法。

## API

| 参数       | 说明           | 类型             | 默认值       |
|------------|----------------|------------------|--------------|
| value    | 对话框是否可见 | boolean          | 无           |
| confirmLoading | 确定按钮 loading | boolean    | 无           |
| title      | 标题           | string\|vnode | 无           |
| closable   | 是否显示右上角的关闭按钮 | boolean    | true        |
| onOk       | 点击确定回调       | function(e)     | 无           |
| onCancel   | 点击遮罩层或右上角叉或取消按钮的回调  | function(e)  | 无         |
| width      | 宽度           | string\|number | 520           |
| footer     | 底部内容，当不需要默认底部按钮时，可以设为 `footer={null}` | string\|vnode | 确定取消按钮 |
| okText     | 确认按钮文字    | string           | 确定       |
| cancelText | 取消按钮文字    | string           | 取消       |
| maskClosable | 点击蒙层是否允许关闭 | boolean   | true       |
| style | 可用于设置浮层的样式，调整浮层位置等 | object   | - |
| wrapClassName | 对话框外层容器的类名 | string   | - |
| afterClose | Modal 完全关闭后的回调 | function | 无 |

### $modal.xxx()

包括：

- `$modal.info`
- `$modal.success`
- `$modal.error`
- `$modal.warning`
- `$modal.confirm`

以上均为一个函数，参数为 object，具体属性如下：

| 参数       | 说明           | 类型             | 默认值       |
|------------|----------------|------------------|--------------|
| title      | 标题           | string\|vnode | 无           |
| content    | 内容           | string\|vnode | 无           |
| onOk       | 点击确定回调，参数为关闭函数     | function         | 无           |
| onCancel   | 取消回调，参数为关闭函数       | function         | 无           |
| width      | 宽度           | string\|number | 416           |
| iconType   | 图标 Icon 类型    | string | question-circle |
| okText     | 确认按钮文字    | string           | 确定       |
| cancelText | 取消按钮文字    | string           | 取消       |
| maskClosable | 点击蒙层是否允许关闭 | Boolean   | `false`    |

<style>
.code-box-demo .ant-btn {
  margin-right: 8px;
}
</style>
