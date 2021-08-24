# ustc-passport-login
登录ustc身份认证系统，可以自动识别验证码
# 使用说明
```
from ustclogin import Login
login=Login(stuid,password,origin,service,exam) #stuid:学号 password:密码 origin:原本想进的网页 service：服务（参见重定向后网址的查询参数） exam:登录成功会自动进去的网页
cookies=login.cookies
result=login.result #登录成功后的页面信息，result.txt即为页面源代码
session=login.session #会话信息
```
# 示例
```
login=Login('PB20000000','******','https://weixine.ustc.edu.cn/2020','https://weixine.ustc.edu.cn/2020/caslogin','https://weixine.ustc.edu.cn/2020/home')#登录健康打卡系统
```
