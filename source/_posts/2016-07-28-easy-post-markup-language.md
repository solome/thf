---
layout: post
title: "给自己的博客文章穿上美丽的外衣"
description: "编辑HTML标签是件及其繁琐的事情，做些配置让编辑文章变得简单容易。"
date: 2016-07-28 16:39:18
comments: true
keywords: "markdown, latex, mathjax"
category: rule
tags:
- markdown
- latex
- mathjax
---

编辑`HTML`标签是件及其繁琐的事情，做些配置让编辑文章变得简单容易。當然，基本語法自然採用[Markdown](http://daringfireball.net/projects/markdown/)，下面僅對一些特殊場景做些簡單說明。


### 源代碼

放置一段`ruby`源碼，效果如下：

```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
```

如果想顯示如上效果，你可以這樣寫：

  ```ruby
  def print_hi(name)
    puts "Hi, #{name}"
  end
  print_hi('Tom')
  #=> prints 'Hi, Tom' to STDOUT.
  ```

也能這樣寫（顯示效果是相似的）：

{% highlight text %}
{% raw %}{% highlight ruby %}{% endraw %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% raw %}{% endhighlight %}{% endraw %}
{% endhighlight %}

### 帶入數學公式

比如經典的[傅立叶变换](https://zh.wikipedia.org/wiki/%E5%82%85%E9%87%8C%E5%8F%B6%E5%8F%98%E6%8D%A2)公式：

$$\widehat{f}(t) =  \int_{-\infty}^{\infty} f(x) e^{-2\pi ixt}dx$$

這種公式效果可以通過
[<b><span lang="en">L<span style="font-variant: small-caps; margin-left: -0.3em; vertical-align: 0.33ex; line-height: 0; margin-right: -0.1em">a</span>T<span style="text-transform: uppercase; margin-left: -0.1667em; vertical-align: -0.5ex; line-height: 0; margin-right: -0.125em">e</span>X</span></b>](https://www.latex-project.org/)的語法來實現（使用`$$`包裹）：

```
$$\widehat{f}(t) =  \int_{-\infty}^{\infty} f(x) e^{-2\pi ixt}dx$$
```

這樣就可以在博客中添加數學相關的公式了。

