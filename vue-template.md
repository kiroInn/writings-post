## custom template

# what is template
数据（变量）到实际的视觉表现（HTML代码）

## 模板解决方案

2jsp/php
1mustcache
3attribute bind

## how to implements

字符串模板变成 ast，
ast 变成模板函数

模板的 html 结构进行解析
变成一颗附带结构、关系、属性的抽象树
DSL.render(templateStr, data);

Ast 生成
1.正则
2.create DOM 解析DOM节点

render函数最后会返回一个VNode节点，在_update的时候，
经过patch与之前的VNode节点进行比较，得出差异后将这些差异渲染到真实的DOM上。





