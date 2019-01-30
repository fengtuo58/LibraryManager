# LibraryManager
一、请实现以下需求：


二、题目内容：

实现一个图书信息管理服务程序，程序支持读取和保存图书信息。

请实现基于HTTP的REST server的2个接口：

* PUT /api/v1/books/<book_id>：表示覆盖一本书的信息，新的书本信息在HTTP BODY中，必须是json格式。
* GET /api/v1/books/<book_id>：表示获取一本书的信息，返回的书本信息是json格式，内容与先前PUT接口设定的信息相同。如果不存在这本书，应该返回404错误。

其中book_id是一个长度不超过19字节的数字文本，如23122311762、1234567890123456781。book_id号并不连续。
书的信息请保存在磁盘文件中，每本书保存一个文件。要求支持管理至少200万本书的信息。
每本书的信息是json格式文本，典型大小是2kbytes。
已知10%的图书是热门图书，对热门图书的查询占到查询量的80%。

要求：
1、PUT接口的单机QPS = 1，GET接口的单机QPS = 2000。
2、服务器上安装的硬盘是普通2T的机械硬盘。
3、不能依赖任何外部数据库。
4、进程内存开销不允许超过800Mbytes。
5、代码实现时只有http web server和json相关代码可以使用库，其他需求均需要使用语言原生功能实现。
6、代码规范、异常处理、可测试性等都是评分的一部分。
7、请使用以下语言之一实现：C、C++、Golang。
2019 01 29
