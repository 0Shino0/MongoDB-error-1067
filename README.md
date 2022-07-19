# MongoDB-error-1067
MongoDBServer无法启动error:1067。保留数据的同时解决问题，两种解决方案。


## 解决方案一:
删除journal文件
清除mongod.lock和storage.bson
重新启动服务

如果上面的无法实现 ,可以尝试下面的
删除服务 
sc delete mongodb
删除journal文件
清除mongod.lock和storage.bson
MongoDB服务删除并重新安装，
再尝试就发现已经可以正常启动了。

## 解决方案二(个人认为较优解):
利用官方安装包修复功能
以mongodb4.4.15为例
打开对应版本的安装包

![image-20220719155339365](http://shinoimg.yyshino.top/img/202207191553716.png)

选中`Repair`进行修复

![image-20220715223953968](http://shinoimg.yyshino.top/img/202207152240327.png)
等待修复完成即可

## 其他问题
目前使用无其他问题
如果有问题请在Issues中讨论
