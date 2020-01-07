# functional-programming

## 一、几个概念区分

### Algebraic Structures(代数结构)

- **templates for solving a problem**
- Algebraic Structures are a bit like code design patterns. Unlike design patterns though, they have mathematical basis and are interrelated. Hence why they're called 'algebraic'. Also, unlike design patterns, they have confusing names made up by mathematicians.
- 常用模式
  - functor模式
    - 将一个单参纯函数提升到一个上下文中
    - List[A], 将f应用到上下文List中，得到List[A'] => List[B']
    - 
  - applicative模式
    - 将一个多参纯函数提升到一个上下文中，中途遇错也继续走
  - monad模式
    - 将一个多参纯函数提升到一个上下文中，中途遇错则停止
  - monoid模式
    - 包含 initValue + combine function
    - 广群(集合S+封闭运算*) -> 半群(+结合律) -> 幺半群(+幺元)
    - 定义了一种在特定场景下将元素合并的标准方法
    - 结合性的保证 可以用来定义函数之间的组合
    - [参考链接](https://blog.csdn.net/JasonDing1354/article/details/50761917)

### Type classes(类型类)

- **a way of doing polymorphism**
- Type classes are a way of implementing polymorphism. They're used in statically typed languages like Haskell or PureScript. They let you define functions with the same name but different type signatures. They're often used to implement algebraic structures. So sometimes people use the terms interchangeably.
- 为已有类型增加功能

### Algebraic Data Types(ADT,代数数据类型)

- **type that's formed by composing other types**
- Algebraic data types are not the same as algebraic structures. What are they? They’re composite data types made out of other types. There’s two main kinds of algebraic data types: Sum types and Product types. Together, they’re like a dynamic duo for encoding business logic. They help us make good things possible, and bad things impossible.

## 建模