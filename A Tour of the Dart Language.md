# Dart语言之旅

此页面向您展示如何使用Dart的主要特征，从变量和运算符到类和库，假设您已经知道如何使用其他语言编程。

想要学习更多的Dar的核心库，可以参考[Dart核心库教程][1]。无论何时您想了解有关语言功能的更多详细信息，请参阅[Dart语言规范][2]。

> Tip: 你可以学习Dart语言特征使用DartPad。[打开DartPad][3]

## Dart的基本使用

下面的代码使用了Dart的最基本的特征

```
// 定义一个函数
printInteger(int aNumber) {
  print('The number is $aNumber.'); // 打印到控制台
}

// 程序执行入口
main() {
  var number = 42; // 声明并初始化一个变量
  printInteger(number); // 调用函数
}
```

以下是此程序使用的适用于所有（或几乎所有）Dart应用程序的内容：

	// 这是一行注释

单行注释，Dart也支持多行注释，与Java注释是类似

	int

数据类型，其他的内置的数据类型，如`String`，`List`，`bool`。

	42

一个字面数字。数字文字是一种编译时常量。

	print()

输出函数，会将需要打印的内容输出到控制台

	'....'或者"...."

字符串

	$variableName或者${expression}

字符串插值：包括字符串文字内部的变量或表达式的字符串。有关更多信息，请参阅[String][4]。

	main()

App执行主要入口，更多信息参考[The main() function][5]

	var

声明变量但不指定类型的关键字

> 注:此网站代码遵循[Dart代码规范指南][6]


## 重要原则

在你学习Dart语言时候，请牢记一下事实和原则

* 您可以放在变量中的所有内容都是一个对象，每个对象都是一个类的实例。甚至数字，函数和`null`都是对象。所有对象都从`Object`类继承。

* 尽管Dart是强类型的。但类型定义是可选的，因为Dart可以推断类型。在上面的代码中，数字被推断为`int`类型。如果要明确说明不指定类型，请使用特殊类型`dynamic`。

* Dart支持泛型类型，例如`List<int>`或`List< dynamic>`


## 关键字



[1]: https://www.dartlang.org/guides/libraries/library-tour
[2]:https://www.dartlang.org/guides/language/spec
[3]:https://dartpad.dartlang.org/
[4]:https://www.dartlang.org/guides/language/language-tour#strings
[5]:https://www.dartlang.org/guides/language/language-tour#the-main-function
[6]:https://www.dartlang.org/guides/language/effective-dart/style