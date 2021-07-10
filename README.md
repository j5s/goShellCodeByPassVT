# goShellCodeByPassVT

## 一丶公众号文章
[Go编译-race参数实现VT全免杀](https://mp.weixin.qq.com/s/GrS6Kf7ZTDHT6cz_W1flfw)

## 二丶命令

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


## 三丶免杀情况
截至2021/7/10 幸免于世
![image-20210710145910623](https://typora-mine.oss-cn-beijing.aliyuncs.com/typora/image-20210710145910623.png)
