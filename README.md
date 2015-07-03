# test_sup
supervisor行为的分析与实践
# 用法
启动引用程序
```
application:start(test_sup).
```
添加子节点
```
my_handle:add_child(add1).
my_handle:add_child(common).
my_handle:add_child(add_sup).    %%添加子监控树，重启策略simple_one_for_one
my_handle:add_child(add2).       %%动态添加子监控树的子进程
my_handle:add_child(add2).
my_handle:add_child(add2).
my_handle:add_child(add2).
```
可视化监控树
```
observer:start().
```
