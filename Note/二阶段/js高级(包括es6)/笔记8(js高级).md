# 上课笔记

### JS高级

+ 作用域
```
    <!-- 
        在运行代码的时候、特定部分中的变量、函数和对象的可访问性，决定变量的可见性 
        作用域就是一个独立的地盘，让变量不外泄、不暴露
        作用：隔离变量，不同作用域下，同名变量不冲突
    -->
    1、全局作用域
        最外层函数外部定义的变量（var x=1）：相当于定义了window的属性
        所有未定义直接赋值的变量（包括在函数内部 x=1）
        window对象的属性，拥有全局作用域（包括在函数内部 window.x=1）
    2、函数作用域(有父子作用域，会从里往外找)


    <!-- 自执行函数：(function(形参){})(实参) -->
```

+ undefine补充
```
    出现undefined的情况
    1、定义了变量未赋值；
    2、对象没有对应属性的
    3、超出数组长度的
    4、调用函数，函数没有返回值的
    5、函数的形参没有接收到实参的时候
```

+ 作用域链
```
    函数作用域(有父子作用域，会从里往外找)
```

+ 变量提升
```
    A、当JS引擎 读到 var/函数声明的时候，会将其提升到("当前")作用域的顶端。
    B、当函数声明的函数名，与var变量名相同时，函数声明优先级更高(不包括匿名函数)
    C、有名字的函数表达式，这个名字不会进入名字空间，这个名字只能在函数内部使用，外面任何地方都不使用
    D、优先级：函数声明>函数参数>var
```

+ 闭包
```
概念：    
    闭包是一个拥有许多变量和绑定了这些变量的环境的表达式（通常是一个函数）
    是指：有权访问另一个函数作用域中的变量的函数
    方式：一个函数内部创建另一个函数，通过另一个函数访问这个函数的局部变量

三个特性：
    1、函数嵌套函数
    2、函数内部可以引用外部的参数和变量
    3、参数和变量不会被垃圾回收机制回收

垃圾回收机制：
    1、JS中，如果一个对象不再被引用，那么这个对象就会被GC（garbage collection）回收
    2、如果两个对象相互引用，而不被第3者引用，那么这两个相互引用的对象也会被回收
```

   
