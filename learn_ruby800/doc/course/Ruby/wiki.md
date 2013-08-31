---
title: 'Ruby百科'

authors:
- master

datetime: '2013-08-31 17:25'

tags:
- ruby
- wiki

categories:
- 百科
- Wiki

outline: 'Ruby，一种为简单快捷的面向对象编程（面向对象程序设计）而创的脚本语言，在20世纪90年代由日本人松本行弘（まつもとゆきひろ /Yukihiro Matsumoto）开发，遵守GPL协议和Ruby License。它的灵感与特性来自于 Perl、Smalltalk、Eiffel、Ada 以及 Lisp 语言。由 Ruby 语言本身还发展出了JRuby（Java 平台）、IronRuby（.NET 平台）等其他平台的 Ruby 语言替代品。Ruby的作者于1993年2月24日开始编写Ruby，直至1995年12月才正式公开发布于fj（新闻组）。因为 Perl发音与6月诞生石pearl（珍珠）相同，因此Ruby以7月诞生石ruby（红宝石）命名。'

---

# 历史

Ruby[1]明显比其他类似的编程语言（如Perl或Python）年轻，又因为Ruby是日本人发明的，所以早期的非日文资料和程序都比较贫乏，所以现在在网上仍然可以找到 Ruby的资料太少之类的批评。约于2000年，Ruby开始进入美国，英文的资料开始发展。

![Ruby标识](/static/images/course/language/ruby/ruby标识1.jpg)

*  2011年10月31日1.9.3的第一个稳定版本1.9.3p0发布。
*  2013年2月22日发布了Ruby 1.9.3-p392。[2]
*  2013年2月24日发布了Ruby 2.0.0-p0。[3]

# 理念

减少编程时候的不必要的琐碎时间，令编写程序的人高兴，是设计 Ruby 语言的 Matz 的一个首要的考虑；其次是良好的界面设计。他强调系统设计必须注重人性化，而不是一味从机器的角度设想。

“ 人们特别是电脑工程师们，常常从机器着想。他们认为：‘这样做，机器就能运行的更快；这样做，机器运行效率更高；这样做，机器就会怎样怎样怎样。’实际上，我们需要从人的角度考虑问题，人们怎样编写程序或者怎样使用机器上应用程序。我们是主人，他们是仆人。 ”

遵循上述的理念，Ruby 语言通常非常直观，按照编程人认为它应该的方式运行。

Ruby 是完全面向对象的：任何一点数据都是对象，包括在其他语言中的基本类型（比如：整数，布尔逻辑值），每个过程或函数都是方法。

下面是一个在标准输出设备上输出Hello World的简单程序，这种程序通常作为开始学习编程语言时的第一个程序：

```ruby
#!/usr/bin/env ruby
puts "Hello, world!"
```

# 特点

Ruby语言中，任何东西都是对象，包括其他语言中的基本数据类型，比如整数。

变量没有类型。

Ruby的变量可以保有任何类型的数据。

任何东西都有值。

不管是数学或者逻辑表达式还是一个语句，都会有值。

# 规则
Ruby的变量有一定的规则，以$开头的一定是全局变量，以@开头的都是实例变量，而以@@开头的是类变量。常数则以大写字母开头；这种方法，对文本编辑器的命令补全很有帮助，如在vim下先键入$及开头字母，再敲击Ctrl+p，则可专门补全本文件以及关联文件中的全局变量，perl与php亦有此优点。

已经定义的类可以在运行时修改。

Ruby是动态语言，你可以在程序中修改先前定义过的类。 也可以在某个类的实例中定义该实例特有的方法，这叫做单例方法。

```ruby
class MyClass
  def the_method
    "general method"
  end
end

mc = MyClass.new

def mc.the_method
  "special for this instance."
end

mc.the_method #special for this instance
```

使用Ruby可以写出简短而又功能强大的代码

```ruby
# 下面的方法用来完成两个矩阵的乘积
def matrix_mul matrix1, matrix2
  result = []

  (0...matrix1.length).each {|i|
    temp = []

    (0...matrix2[0].length).each { |j|
      tmp = 0
      (0...matrix1[0].length).each { |k|
        tmp += matrix1[i][k]*matrix2[k][j]
      }
      temp << tmp
    }

    result << temp
  }

  return result
end
```
注：ruby标准库中已包含矩阵库 Matrix

# 优点

* 语法简单
* 普通的面向对象功能(类,方法调用等)
* 特殊的面向对象功能(Mixin,特殊方法等)
* 操作符重载
* 错误处理功能
* 迭代器和闭包
* 垃圾回收
* 动态载入(取决于系统架构)
* 可移植性高.不仅可以运行在多数UNIX上,还可以运行在DOS,Windows,Mac,BeOS等平台上
* 适合于快速开发，一般开发效率是JAVA的5倍

# 作者

松本行弘"Matz"(Matsumoto Yukihiro)是Ruby语言的发明人，他从1993年起便开始着手Ruby的研发工作。他一直想发明一种语言，使你既能进行高效开发又能享受编程的快乐。1993年2月24日Ruby诞生了，1995年12月Matz推出了Ruby的第一个版本Ruby 0.95。不久Ruby便凭借其独特的魅力横扫日本，相信在不久的将来，Ruby将走向世界。

# 参考资料

* [百度百科](http://baike.baidu.com/view/45135.htm)
