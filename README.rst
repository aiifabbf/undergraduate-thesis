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