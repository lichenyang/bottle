.. image:: http://bottlepy.org/docs/dev/_static/logo_nav.png
  :alt: Bottle Logo
  :align: right

.. _mako: http://www.makotemplates.org/
.. _cheetah: http://www.cheetahtemplate.org/
.. _jinja2: http://jinja.pocoo.org/
.. _paste: http://pythonpaste.org/
.. _fapws3: https://github.com/william-os4y/fapws3
.. _bjoern: https://github.com/jonashaag/bjoern
.. _cherrypy: http://www.cherrypy.org/
.. _WSGI: http://www.wsgi.org/
.. _Python: http://python.org/

============================
Bottle: Python编写的Web框架
============================

Bottle是一个由 Python_ 编写， 高性能、 简单且轻量级的 WSGI_ 小型框架。他是一个单一的 Python_ 模块，因此不依赖与任何其他的 `Python标准程序库 <http://docs.python.org/library/>`_.


* **路由:** 通过Bottle内建的路由，请求被映射为函数调用，而且它还支持用户友好的URL甚至动态URL。 
* **模板:** Bottle `*内建* <http://bottlepy.org/docs/dev/tutorial.html#tutorial-templates>`_ 了高性能的模板引擎同时他还支持 mako_, jinja2_ 和 cheetah_。
* **工具:** 通过Bottle可以很方便的访问表单数据, 上传文件, 调整Cookies, 以及发送Http头。
* **服务器:** 可以通过自带的HTTP Server以及 paste_, fapws3_, bjoern_, `Google App Engine <http://code.google.com/intl/en-US/appengine/>`_, cherrypy_ 等 WSGI_ HTTP Server运行Bottle编写的应用。

项目主页: http://bottlepy.org


例子: Bottle的"Hello World"
---------------------------

.. code-block:: python

  from bottle import route, run, template

  @route('/hello/<name>')
  def index(name):
      return template('<b>Hello {{name}}</b>!', name=name)

  run(host='localhost', port=8080)

运行这段代码或者将其拷贝到Python控制台中, 用浏览器打开 `<http://localhost:8080/hello/world>`_。 大功告成！


下载和安装
----------

.. __: https://github.com/defnull/bottle/raw/master/bottle.py

你可以通过 ``pip install bottle``, ``easy_install -U bottle`` 来安装最新的稳定版本，或者下载 `bottle.py`__ (不稳定) 到你的工程目录下。 它对你的Python没有太高要求，只需要 **Python 2.5+ and 3.x**。


声明
----

.. __: https://github.com/defnull/bottle/raw/master/LICENSE

本文是基于Bottle原文档的中文译本。

代码和文档遵循 MIT License (see LICENSE__)。

Bottle的Logo并不适用该协议。使用前必须向作者征求意见。
