
## HTML5 新增语义化标签有哪些？作用？
- `<header>`、`<nav>`、`<main>`、`<article>`、`<section>`、`<aside>`、`<footer>`  
- 作用：提升代码可读性、利于 SEO、增强可访问性（屏幕阅读器识别结构）。

---

## CSS 盒模型组成？`box-sizing` 两种值的区别？
- 组成：`content` + `padding` + `border` + `margin`  
- `content-box`（默认）：width/height 只包括 content 区域。  
- `border-box`：width/height 包括 content + padding + border，便于布局计算。

---

## BFC 触发条件与应用场景？
- 触发条件：浮动元素、`position: absolute/fixed`、`overflow` 不为 `visible`、`display: inline-block / flex / grid` 等。  
- 应用场景：清除浮动、避免外边距合并、隔离布局防止干扰。

---

## Flex 主轴与交叉轴对齐方式的常用属性？
- 主轴：`justify-content`（flex-start | center | space-between ...）  
- 交叉轴：`align-items`（单行）、`align-content`（多行）

---

## position 各值及特点？
- `static`：默认定位，不受 top/left 影响。  
- `relative`：相对自身原位置偏移，不脱离文档流。  
- `absolute`：相对最近的定位祖先（非 static）定位，脱离文档流。  
- `fixed`：相对视口定位，不随滚动变化。  
- `sticky`：在滚动到设定阈值前为 relative，之后为 fixed。

---

## HTML 表单中 `input` 的 `type` 有哪些常用值？语义与用途？
- `text`：单行文本  
- `password`：密码框（掩码显示）  
- `email` / `tel` / `url`：带格式校验的输入类型  
- `number`：数字输入（可设 min/max/step）  
- `date` / `time` / `datetime-local`：日期时间选择  
- `checkbox` / `radio`：多选/单选  
- `file`：文件上传  
- `submit` / `reset` / `button`：按钮控件  
- 作用：提高可用性、启用移动端优化键盘、原生校验。

---

## HTML 如何实现图片懒加载？语义与性能意义？
- 原生：`loading="lazy"`（img 标签属性）  
- 兼容方案：JS 监听 `IntersectionObserver` 替换 `src`  
- 意义：减少首屏请求数、降低带宽消耗、加快初始渲染速度。

---

## CSS 选择器优先级计算规则？
- 内联 style（1000） > ID（100） > Class/伪类/属性（10） > 元素/伪元素（1） > 通配符（0）  
- 同优先级按出现顺序，后出现覆盖先出现。  
- `!important` 强制最高优先级（慎用）。

---

## 如何实现水平垂直居中？（至少 3 种方法）
1. Flex：`display: flex; justify-content: center; align-items: center;`  
2. Grid：`display: grid; place-items: center;`  
3. Position + Transform：`position: absolute; top:50%; left:50%; transform: translate(-50%, -50%);`  
4. Table-Cell：`display: table-cell; vertical-align: middle; text-align: center;`

---

## CSS 层叠上下文（Stacking Context）形成条件？z-index 失效原因？
- 形成条件：`position` 非 static 且 z-index 有值、`opacity < 1`、`transform`/`filter`/`will-change` 等。  
- z-index 失效：元素未创建层叠上下文，与父级或其他层叠上下文比较时层级受限。

---

## CSS 动画与过渡的区别？性能注意点？
- Transition：状态 A → B 的平滑变化，需触发（如 hover）  
- Animation：可定义关键帧序列，自动循环播放  
- 性能注意：优先使用 `transform` 与 `opacity` 做动画，触发 GPU 加速，避免触发布局（layout）与重绘（paint）。

---

## 响应式布局常用方案？
- 媒体查询 `@media`  
- 百分比 / vw / vh 单位  
- 弹性布局 Flexbox  
- 网格布局 Grid  
- 图片自适应 `max-width: 100%`  
- 移动优先或断点设计思路。

---

## CSS 隐藏元素的几种方法及区别？
- `display: none`：元素不占空间，无法交互，不参与渲染树。  
- `visibility: hidden`：元素占空间，不可见，保留渲染树节点。  
- `opacity: 0`：元素占空间，可交互（透明），仍在渲染树。  
- `position: absolute; left: -9999px`：视觉移出可视区，保留占位与可访问性。

---

## HTML 无障碍（a11y）常用做法？
- 使用语义化标签（header/nav/main/article…）  
- 为图片加 `alt` 描述  
- 表单加 `label` 关联 `input`（for/id）  
- 保证键盘可导航（tabindex）  
- 对比度符合 WCAG 标准  
- ARIA 属性补充语义（role、aria-*）。