# ustc-passport-login
登录ustc新版身份认证系统，可以自动识别验证码
# 使用说明
登录部分已包装成Login类，使用时导入即可
```python
from ustclogin import Login
login=Login(stuid,password,service) #stuid:学号 password:密码 service：服务（参见重定向后网址的查询参数）
cookies=login.cookies
result=login.result #登录成功后的页面信息，result.text即为页面源代码
session=login.session #会话信息
```
# 示例
```python
login=Login('PB20000000','******','https://weixine.ustc.edu.cn/2020/caslogin')#登录健康打卡系统
#Login返回True表示登录成功，否则登录失败
```
修改后的自动健康打卡脚本：https://github.com/Kobe972/USTC-ncov-AutoReport
