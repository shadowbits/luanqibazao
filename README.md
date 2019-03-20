# 代理设置
在macos 中经常遇到一个问题"代理"。在网络中设置的代理是可以被浏览器使用的。但是终端无法使用。

这里我们可以设置全局代理：代码如下 具体的IP和端口根据实际情况设置
----

alias proxy='export all_proxy=socks5://127.0.0.1:1080'

alias noproxy='unset all_proxy'

----
将这个两行添加在当前用户目录下(~)的.bash_profile文件中。

当需要开启全局代理时直接输入命令：proxy 
不需要时输入命令：noproxy
[notice] 注意这个代理只会被当前打开的终端使用，其他终端或软件理论上是不会走这个代理的。这种方式保证了proxy的最小污染，只有当你需要的时候使用即可。
