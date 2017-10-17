kdcx.py
========

利用kuaidi100.com网站提供的api进行快递单进度查询的小程序。

安装
=======

..  bash命令:

    $ pip install kd100

用法
=====

``kd100``: 普通用法，在命令行输入快递单号，回车后返回快递信息。

``kd100 -c code``: ``-c`` 意为code, 指定的快递代码.

``kd100 -c code -o filename``: ``-o`` 表示output，指定输出文件名。

``kd100 -c code -o filename -p company_name``: ``-p`` 是company,指公司，指定快递公司名称，自动猜测错误时有用。

输入 ``kd100 -h`` 获取帮助。

示例
=======

..  code:: bash

    yourname@computer:~$ kd100
    Input your express code: <Your code>
    Possible company: zhongtong, kuayue, yuantong, zhaijisong, shengfengwuliu
    Try zhongtong ...Done
    code: <Your  code>         company: zhongtong       is checked: 0
    =================================================================
            time         |                  content
    -----------------------------------------------------------------
     2015-08-16 17:40:28 | first content
    -----------------------------------------------------------------
     2015-08-16 17:02:32 | some content
    -----------------------------------------------------------------
    ...
    -----------------------------------------------------------------
     2015-08-13 20:41:27 | last content
    =================================================================

..  image:: http://ww4.sinaimg.cn/large/88e401f0gw1evjtouw9hgj20m20cnjyl.jpg

更新日志
=========

- v0.0.5

  - express code should no long be numbers, to support company like APELAX

- v0.0.4

  - remove third party module dependencies.
  - add ``-p`` option to specified company.

- v0.0.2

  - kuaidi100 webside change the rule, need special header referer when send query

- v0.0.1

  - first version, with base function.

LICENSE
=======

MIT.
