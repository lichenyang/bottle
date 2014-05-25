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


Example: "Hello World" in a bottle
----------------------------------

.. code-block:: python

  from bottle import route, run, template

  @route('/hello/<name>')
  def index(name):
      return template('<b>Hello {{name}}</b>!', name=name)

  run(host='localhost', port=8080)

Run this script or paste it into a Python console, then point your browser to `<http://localhost:8080/hello/world>`_. That's it.


Download and Install
--------------------

.. __: https://github.com/defnull/bottle/raw/master/bottle.py

Install the latest stable release with ``pip install bottle``, ``easy_install -U bottle`` or download `bottle.py`__ (unstable) into your project directory. There are no hard dependencies other than the Python standard library. Bottle runs with **Python 2.5+ and 3.x**.


License
-------

.. __: https://github.com/defnull/bottle/raw/master/LICENSE

Code and documentation are available according to the MIT License (see LICENSE__).

The Bottle logo however is *NOT* covered by that license. It is allowed to use the logo as a link to the bottle homepage or in direct context with the unmodified library. In all other cases please ask first.
