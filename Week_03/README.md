学习笔记

# ll构建语法树（AST）
ll: l = left
## 四则运算包括
1. TokenNumber —— 数字输入
2. 1 2 3 4 5 6 7 8 9 0 的组合 (允许在数字中间插入小数点)
3. Operator (+、-、*、/ 之一) —— 加减乘除运算符
4. Whitespace (<sp>) —— 空格
5. LineTerminator (<LF> <CR>) —— 换行
分为词法分析和语法分析

# yield
yield是ES6的新关键字，使生成器函数执行暂停，yield关键字后面的表达式的值返回给生成器的调用者。它可以被认为是一个基于生成器的版本的return关键字。
yield关键字实际返回一个IteratorResult（迭代器）对象，它有两个属性，value和done，分别代表返回值和是否完成。
yield无法单独工作，需要配合generator(生成器)的其他函数，如next，懒汉式操作，展现强大的主动控制特性。

如果看到某个函数中有yield，说明这个函数已经是个生成器了
yield可以用来加强控制，懒汉式加载
调用函数指针和调用生成器是两码事，注意上面的运行结果，countAppleSales和myArr。
需要next()函数配合使用，每次调用返回两个值：分别是value和done，代表迭代结果和是否完成
函数next()是个迭代器对象，传参可以缺省，默认调用函数
