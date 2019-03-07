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

下面的这个表格列出了Dart语言专门的关键词

<table class="table table-striped nowrap">
  <tbody>
    <tr>
      <td>
<a href="#abstract-classes">abstract</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#important-concepts">dynamic</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#implicit-interfaces">implements</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#importing-only-part-of-a-library">show</a>&nbsp;<sup title="contextual keyword" alt="contextual keyword">1</sup>
</td>
    </tr>
    <tr>
      <td>
<a href="#type-test-operators">as</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td><a href="#if-and-else">else</a></td>
      <td>
<a href="#using-libraries">import</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#class-variables-and-methods">static</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
    </tr>
    <tr>
      <td><a href="#assert">assert</a></td>
      <td><a href="#enumerated-types">enum</a></td>
      <td><a href="#for-loops">in</a></td>
      <td><a href="#extending-a-class">super</a></td>
    </tr>
    <tr>
      <td>
<a href="#asynchrony-support">async</a>&nbsp;<sup title="contextual keyword" alt="contextual keyword">1</sup>
</td>
      <td>
<a href="/guides/libraries/create-library-packages">export</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="https://stackoverflow.com/questions/28595501/was-the-interface-keyword-removed-from-dart" class="external">interface</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td><a href="#switch-and-case">switch</a></td>
    </tr>
    <tr>
      <td>
<a href="#asynchrony-support">await</a>&nbsp;<sup title="limited reserved word" alt="limited reserved word">3</sup>
</td>
      <td><a href="#extending-a-class">extends</a></td>
      <td><a href="#type-test-operators">is</a></td>
      <td>
<a href="#generators">sync</a>&nbsp;<sup title="contextual keyword" alt="contextual keyword">1</sup>
</td>
    </tr>
    <tr>
      <td><a href="#break-and-continue">break</a></td>
      <td>
<a href="https://stackoverflow.com/questions/24929659/what-does-external-mean-in-dart" class="external">external</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#libraries-and-visibility">library</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td><a href="#constructors">this</a></td>
    </tr>
    <tr>
      <td><a href="#switch-and-case">case</a></td>
      <td>
<a href="#factory-constructors">factory</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#adding-features-to-a-class-mixins">mixin</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td><a href="#throw">throw</a></td>
    </tr>
    <tr>
      <td><a href="#catch">catch</a></td>
      <td><a href="#booleans">false</a></td>
      <td><a href="#using-constructors">new</a></td>
      <td><a href="#booleans">true</a></td>
    </tr>
    <tr>
      <td><a href="#instance-variables">class</a></td>
      <td><a href="#final-and-const">final</a></td>
      <td><a href="#default-value">null</a></td>
      <td><a href="#catch">try</a></td>
    </tr>
    <tr>
      <td><a href="#final-and-const">const</a></td>
      <td><a href="#finally">finally</a></td>
      <td>
<a href="#catch">on</a>&nbsp;<sup title="contextual keyword" alt="contextual keyword">1</sup>
</td>
      <td>
<a href="#typedefs">typedef</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
    </tr>
    <tr>
      <td><a href="#break-and-continue">continue</a></td>
      <td><a href="#for-loops">for</a></td>
      <td>
<a href="#overridable-operators">operator</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td><a href="#variables">var</a></td>
    </tr>
    <tr>
      <td>
<a href="/guides/language/sound-problems#the-covariant-keyword">covariant</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#functions">Function</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="/guides/libraries/create-library-packages#organizing-a-library-package">part</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td><a href="https://medium.com/dartlang/dart-2-legacy-of-the-void-e7afb5f44df0" class="external">void</a></td>
    </tr>
    <tr>
      <td><a href="#switch-and-case">default</a></td>
      <td>
<a href="#getters-and-setters">get</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td><a href="#catch">rethrow</a></td>
      <td><a href="#while-and-do-while">while</a></td>
    </tr>
    <tr>
      <td>
<a href="#lazily-loading-a-library">deferred</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#importing-only-part-of-a-library">hide</a>&nbsp;<sup title="contextual keyword" alt="contextual keyword">1</sup>
</td>
      <td><a href="#functions">return</a></td>
      <td><a href="#adding-features-to-a-class-mixins">with</a></td>
    </tr>
    <tr>
      <td><a href="#while-and-do-while">do</a></td>
      <td><a href="#if-and-else">if</a></td>
      <td>
<a href="https://api.dartlang.org/stable/dart-core/Set-class.html" class="external">set</a>&nbsp;<sup title="built-in-identifier" alt="built-in-identifier">2</sup>
</td>
      <td>
<a href="#generators">yield</a>&nbsp;<sup title="limited reserved word" alt="limited reserved word">3</sup>
</td>
    </tr>
  </tbody>
</table>

避免使用这些关键字作为标识符或者变量，然而如果必须使用，带有上标的关键字才可以作为标识符或者变量

*

*

*

其余的关键字都是保留字，不允许作为标识符或者变量


[1]: https://www.dartlang.org/guides/libraries/library-tour
[2]:https://www.dartlang.org/guides/language/spec
[3]:https://dartpad.dartlang.org/
[4]:https://www.dartlang.org/guides/language/language-tour#strings
[5]:https://www.dartlang.org/guides/language/language-tour#the-main-function
[6]:https://www.dartlang.org/guides/language/effective-dart/style