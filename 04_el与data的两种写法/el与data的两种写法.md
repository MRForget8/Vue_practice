# 创建Vue实例从而完成相关代码

```vue
   const v = new Vue({
        data:{
            name: 'atguigu'
        }
    })
    console.log(v)
    v.$mount('#root')
```



这段代码是使用Vue.js创建一个Vue实例，并将其挂载到指定的DOM元素上。

首先，代码使用`const v = new Vue({ ... })`创建一个Vue实例。在Vue实例的选项中，我们可以定义各种属性和方法。在这个例子中，只定义了一个`data`属性，它包含了一个名为`name`的属性，其初始值为字符串`'atguigu'`。

然后，通过`console.log(v)`打印Vue实例。这将显示Vue实例的详细信息，包括其内部状态和选项。

最后，使用`v.$mount('#root')`将Vue实例挂载到具有`id`为`'root'`的DOM元素上。`$mount`是Vue实例的方法，用于手动将实例挂载到DOM元素上。这里的`'#root'`是选择器，指定了要挂载的DOM元素的id。

总结：该代码创建了一个Vue实例，并将其数据属性和方法挂载到具有id为`'root'`的DOM元素上。

# data与el的两种写法

1. el有两种写法
   - new Vue配置el属性
   - 先创建Vue实例，随后再通过vm.$mount/('#root')指定el的值
   
2. data有两种写法
   - 对象式
   - 函数式
   
   如何选择：组件时期，data必须用函数式，否则报错
   
3. 一个重要的原则

   - 由Vue管理的函数，一定不要写箭头函数，一旦写了箭头函数，this就不再是Vue实例了。

