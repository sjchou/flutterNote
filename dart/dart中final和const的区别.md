# Dart中final和congst的区别

它们的区别在于，const比final更加严格。final只是要求变量在初始化后值不变，但通过final，我们无法在编译时（运行之前）知道这个变量的值；而const所修饰的是编译时常量，我们在编译时就已经知道了它的值，显然，它的值也是不可改变的。

``` dart
void main() {
  final name = 'Bob';
  // name = 'job'; //运行出错，因为final修饰的变量不能调用其setter方法，即：不能设值

  const a = 1000000; // 定义常量值
  var b = 100;
  //     const c = b; // 运行出错， const需要在编译时候就知道变量的值

  final c = b;
  // c = 111;// 运行，final不能修改

  const d = a;
}

```
