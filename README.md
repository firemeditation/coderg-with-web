# CoderG #

这是一个用Go语言开发的极简Web和B/S框架。

------

**主要特点**

+ 以“单元”（Unit）的概念对实现某一功能模块的一组控制器的管理；

+ 通过“门口”（UnitDoor）文件对“单元”内控制器进行路由管理；

+ 使用“节点”（Node）和“节点树”（NodeTree）来组织“单元”和路由信息；

+ 通过“节点树”实现直接的全站无限级分类和自动化的路由表生成;

+ 支持HTTP和HTTPS。

------

**局限**

+ 因为本框架的主要目标是放在“单元”和“节点”上，所以并没有针对GET和POST等多方式请求做任何处理，而且也没有的URL的请求返回做过多处理。

+ 因为CoderG开发者本人只在Go下用过PostgreSQL，所以目前CoderG关于数据库连接方面也只为PostgreSQL准备（必须连接），而且没有使用任何ORM，也没有model层。

+ CoderG的功能很单纯，目标很明确，所以不要指望它大而全，什么功能都有。

------

**依赖**

CoderG依赖两个第三方包：

+ github.com/msbranco/goconfig，用来对所有的配置文件进行处理；

+ github.com/lib/pq，PostgreSQL的数据库驱动。

------

**项目网站**

目前项目网站还只有一个临时的访问地址：[CoderG](http://www.ydmsh.com/shift.php?s=12121)。在这里你可以查看文档并提问。

src/codergweb是此项目网站的源代码，你可以在本地编译并运行这个站点，具体操作如下：

+ 使用go get安装上面所说的两个第三方包；

+ 按照src/codergweb中的codergweb.cfg配置文件中关于数据库的配置信息配置好PostgreSQL；

+ 使用database.sql文件的内容建立好数据表；

+ 使用pgAdmin等程序在admins表中添加一个你自己的管理员帐号，其中密码需要sha1加密后的40位全小写字符；

+ 在终端执行build脚本文件，程序将被编译和运行，你可以去bin路径看具体的文件。

------

**其他**

+ coderg/webconfig-example.cfg 文件为示例用的网站配置文件，其中标出“必需”的项目请保证一定要包含在你自己的配置文件中，否则CoderG无法运行。

+ CoderG使用 GNU GPL v3 许可证授权，不喜勿入。
