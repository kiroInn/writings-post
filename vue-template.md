## custom template

# what is template
数据（变量）到实际的视觉表现（HTML代码）

自定义Render函数

Vue.component('anchored-heading', {
      render: function (createElement) {
          return createElement(
              'h' + this.level,   // tag name 标签名称
              this.$slots.default // 子组件中的阵列
          )
      },
      props: {
          level: {
              type: Number,
              required: true
          }
      }
  })
template写法

var vm = new Vue({

  data: {
      // 以一个空值声明 `msg`
      msg: ''
  },
  template: '<div>{{msg}}</div>'
})

el写法（这个就是入门时最基本的写法）

var app = new Vue({

  el: '#app',
  data: {
      message: 'Hello Vue!'
  }



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


## 模板函数
模板函数的构造都大同小异，基本是都是通过拼接函数字符串，
然后通过Function对象转换成一个函数，变成一个函数之后，
只要传入对应的数据，函数就会返回一个模板数据渲染好的 html 字符串。




