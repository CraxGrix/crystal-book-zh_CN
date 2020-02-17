# HTTP 服务器

一个更有趣的例子是HTTP服务器：

```crystal
require "http/server"

server = HTTP::Server.new do |context|
  context.response.content_type = "text/plain"
  context.response.print "Hello world! The time is #{Time.local}"
end

address = server.bind_tcp 8080
puts "Listening on http://#{address}"
server.listen
```

在读完整页教程后我们就能理解上述的代码了，但是现在可以从中发现一些事情。

* 你可以通过 [引入（Require）](../syntax_and_semantics/requiring_files.html) 来引入其他文件里的代码:

    ```crystal
    require "http/server"
    ```
* 你可以定义 [局部变量（local variables）](../syntax_and_semantics/local_variables.html) 且无需指定其具体类型:

    ```crystal
    server = HTTP::Server.new ...
    ```
* 你可以通过调用对象HTTP::Server上的bind_tcp方法设置HTTP服务器的端口（端口设置为8080）
    ```crystal
    address = server.bind_tcp 8080
    ```


* 你可以调用对象的 [方法（methods）](../syntax_and_semantics/classes_and_methods.html) (或发送消息) ：

    ```crystal
    HTTP::Server.new ...
    ...
    Time.local
    ...
    address = server.bind_tcp 8080
    ...
    puts "Listening on http://#{address}"
    ...
    server.listen
    ```

* 你可以使用 [代码块（blocks）](../syntax_and_semantics/blocks_and_procs.html), 这是复用代码的好方法，同时也可以用来模仿函数程序设计的特性:

    ```crystal
    HTTP::Server.new do |context|
      ...
    end
    ```

* 你可以轻松创建带有嵌入内容的字符串，称为**字符串插值**。Crystal还可以通过其他 [语法（syntax）](../syntax_and_semantics/literals.html) 来创建数组，哈希，range, 元组等数据类型:

    ```crystal
    "Hello world! The time is #{Time.local}"
    ```

