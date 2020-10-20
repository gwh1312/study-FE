# 事件循环

## js代码执行机制

+ 所有同步任务都在主线程上的栈中执行
  
+ 主线程之外,还存在一个"任务队列",只要异步任务有了运行结果,就在"任务队列"中放置一个事件

+ 一旦"栈"中的所有同步任务执行完毕,系统就会读取"任务队列",选择出需要首先执行的任务

## 宏任务和微任务

1. 宏任务

2. 微任务

3. 先同步 再取出第一个宏任务执行 所有相关的微任务总会在下一个宏任务之前全部执行完毕 如果遇见 就先微后宏

## 理解

每办完一个业务,柜员就会问当前的客户,是否还有其他需要办理的业务(检查还有没有微任务需要处理)

而客户明确告知说没有事情以后,柜员就去查看后边还有没有等着办理业务的人(结束本次宏任务,检查还有没有宏任务需要处理)