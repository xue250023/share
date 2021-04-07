ES一些新特性
Object.fromEntries().

使二维数组变为对象的形式            使用场景： 解析url参数

?.       可选链操作符                        使用场景： 取对象的属性 obj?.a?.b

??      空值合并操作符                    使用场景： 除去null，undeifined，一些其他假值是可以作为值存在的时候

Array.prototype.flat(param)

扁平化数组，可以进行指定维度的扁平化。

proxy & Reflect || Object.defineProperty


介绍
Reflect

意味 反射，集中了一些操作底层的一些方法，面向函数式编程。

Reflect 不是一个构造函数，所有属性和方法都是静态的。

proxy

代理。

可以拦截对内部对象的访问，在复杂操作前进行校验等。

应用     demo传送门
观察者模式

构造函数取巧

可验证的函数参数



proxy代理不会产生新的内存空间，可以代理整个对象，不需要遍历属性进行设置存取器，可以监听长度的变化