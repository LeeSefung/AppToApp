# AppToApp
# AppToApp

1.假设你现在开发了一个应用A，如果用户机器上已经安装了此应用，并且在应用B中希望能够直接打开A。那么首先需要确保应用A已经配置了Url Types，具体方法就是在plist文件中添加URL types节点并配置URL Schemas作为具体协议.
假设设置为appOne.

2.在应用B中就可以调用openURL方法像打开系统应用一样打开第三方应用程序了.
NSString *url=@"appOne://";
[[UIApplication sharedApplication] openURL:url];
