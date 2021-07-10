# goShellCodeByPassVT
通过线程注入及-race参数免杀全部VT

~~~go
go build -ldflags "-s -w" -race main.go
~~~

其中代码默认注入进程是exploer.exe，位于22行，inProcessName参数。
~~~go
inProcessName    =    "exploer.exe"
~~~

shellcode生成后使用base64编码一次放入**b64body**即可
~~~go
b64body = ""
~~~

### 公众号文章
[Go编译-race参数实现VT全免杀](https://mp.weixin.qq.com/s?src=11&timestamp=1625897670&ver=3181&signature=KPi53pi9YLfS-419yr4Is5uwCxejkeK2Ki0rbrtFZ2occDxV0aycmvxKBjhgQE8pm3m*I7lBYo9jwxYdHfBaQ0fr3-SJAWHaBkF5ait6BvFwzzZSfnPL*xJb0CQhewpm&new=1)
