# car-qrcode-notify
挪车二维码

在大佬的基础上增加了，部分后台管理功能（需要绑定 KV 数据库），可通过 api 添加，删除，更新、查看车辆列表，部署一次可多辆车辆一起使用，无需重复部署。通知发送、获取手机号都由服务器处理，通知渠道支持 WxPusher、Bark、飞书机器人、微信机器人、钉钉机器人、NapCatQQ、Lagrange.Onebot，如需更多渠道可自行增加。可设置发送通知的速率，可设置首页风格。\

【V2.0更新内容】\
1、增加管理后台（车辆管理、用户管理、模板管理、通知管理）需要绑定D1数据库\
2、模板页可使用{{no}}           车牌号、 {{is_notify}}    消息通知、 {{is_call}}      电话通知、 这三个模板变量\

# 正文开始

1、复制 [worker.js](https://github.com/oozzbb/car-qrcode-notify/blob/main/worker.js) 文件内的代码部署到 cloudflare workers 即可\
2、在新建的 workers 的设置中绑定 KV 数据库，具体如下图（变量名称必须为 DATA）\
3、在新建的 workers 的设置中绑定 D1 数据库，具体如下图（变量名称必须为 DB）\
<img width="992" height="149" alt="image" src="https://github.com/user-attachments/assets/ad5589a9-ed35-4d60-b110-cb897bb1e5c0" />
4、在d1数据库控制台执行schema.sql建表命令

# 使用方法

部署完后访问你自己的 workers 即可\
1、https://xxxxxx.workers.dev/login 后台车辆管理登录页面\
2、https://xxxxxx.workers.dev/register 用户注册页面（第一个注册的为管理员账号）

<img width="1912" height="948" alt="image" src="https://github.com/user-attachments/assets/a68ceebc-9e5e-4fda-84f7-0a62063a54f7" />
<img width="1912" height="948" alt="image" src="https://github.com/user-attachments/assets/1f89d676-fc9d-4678-b14f-5813231a800b" />
<img width="1912" height="948" alt="image" src="https://github.com/user-attachments/assets/448c82b0-d810-436c-8c3c-937e95d4d781" />
<img width="1912" height="1199" alt="image" src="https://github.com/user-attachments/assets/c0edf148-0d91-4b28-8374-aab94993e271" />


![1731510826119](https://github.com/user-attachments/assets/eb400783-25f4-49f2-bda7-afba87e0adbd)

![1731591538885](https://github.com/user-attachments/assets/be461088-4769-45ea-b11d-bfe1f7e104c9)

