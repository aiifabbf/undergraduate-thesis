=======
毕业论文
=======

是的没错，sizer_ 就是我的毕设项目。

.. _sizer: https://github.com/aiifabbf/sizer

要求
=====

-   全文15000字以上
-   摘要300字以上
-   参考文献15篇以上
-   外文参考文献4篇以上
-   关键字3-8个

索引
=====

-   全文_

.. _全文: main.rst

生成预览
=======

首先你要有Python，和一个叫做docutils的包。Python安装方法不谈了。docutils的话如果你装过sphinx会作为依赖装好，如果没有装的话，可以用pip装，

.. code:: bash

    pip install docutils

装好之后，

.. code:: bash

    sh build-preview.sh

会在当前目录生成 ``preview.html`` 。打开之后，可以直接看，也可以用浏览器打印出来看哟！

安装 `Latin Modern字体`_ 后风味更佳。

.. _`Latin Modern字体`: http://www.gust.org.pl/projects/e-foundry/latin-modern

正式定稿
=======

因为学校查重只能提交docx，所以最后交给学校的版本还是用pandoc把rst转换成docx、再手动调格式得到的。

有几个坑

-   pandoc不支持rst的citation语法，比如 ``[tan2013]_``

    所以最后参考文献都是我手动加的、手动在文中加入引用标记的。

-   pandoc不会生成图、表的题注，就是 ``图5-3`` 这种

    尽管pandoc会很贴心地会给图、表的caption应用一个类似 ``ImageCaption`` 的样式，但是改那个样式并不能得到类似 ``图5-3`` 这种效果。这种效果要手动一个一个给每个图、表的caption前面加题注。

-   pandoc不认识公式里的 ``\rm, \over``

    所以含有这些的公式我后来手动重新打了。

-   pandoc不会给公式编号

    所以我也是在word里一个一个给公式编号。

    word的公式编号很恶心，要在打完公式之后，在后面插入 ``#()`` 这样一个东西，然后最关键的一步来了，如果你想要得到类似 ``(3-2)`` 的这种效果，肯定会想到用题注，但是直接把光标定位到括号中间 ``#(|)`` 是 **不能插入题注的！** 这个真的非常坑爹，一定要先把公式变成 ``线性`` ，才能在那两个括号中间插入题注。插入题注之后再变回来变成 ``专业型`` 。
    
    此处超级感谢 `@mpraiser <https://github.com/mpraiser>`_ 。

不过好在也没有花很多时间，大概花了一天把格式调好了。

恭喜自己毕业吧，嘻嘻。