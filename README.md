# Module-grammar-of-ES6
ES6中module的语法  
### 严格模式
    ES6模块下自动采用严格模式，不管有没有加入"use-strict".  
    限制主要包括：  
        - 变量必须声明后再用
        - 函数的参数不能有同名属性，否则报错
        - 不能使用 with 语句
        - 不能对只读属性赋值，否则报错
        - 不能使用前缀 0 表示八进制数，否则报错
        - 不能删除不可删除的属性，否则报错
        - 不能删除变量 delete prop，会报错，只能删除属性 delete global[prop]
        - eval 不会在它的外层作用域引入变量
        - eval 和 arguments 不能被重新赋值
        - arguments 不会自动反映函数参数的变化
        - 不能使用 arguments.callee
        - 不能使用 arguments.caller
        - 禁止 this 指向全局变量
        - 不能使用 fn.caller 和 fn.arguments 获取函数调用的堆栈
        - 增加了保留字（比如 protected、static 和 interface）
        - 顶层的this指向undefined，不应该在顶层代码使用this
### export 命令
- 用于规定模块的对外接口
  一个模块就是一个独立的文件，如果想从外部获取该模块的变量，需要使用 export 关键字输出该变量  
```
export var c = "1";  
或者  
var c = "1";  
var b = "2";  
export {c,b};
````
        
### import 命令
- 用于输入其他模块提供的功能
