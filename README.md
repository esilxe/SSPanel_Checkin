## SSPanel_Checkin
[![SSPanel_Checkin](https://github.com/inokoe/SSPanel_Checkin/actions/workflows/main.yml/badge.svg)](https://github.com/inokoe/SSPanel_Checkin/actions/workflows/main.yml)

This is a dish chicken script for automatic check-in of sspanel for GitHub action,
It is only applicable when there is no verification code protection and cloudflare protection, and there is no more perfect exception handling and push.
 
这是一个用于GitHub action 的 sspanel 自动签到的菜鸡脚本,
仅仅适用于没有验证码保护，没有cloudflare保护的情况下，没有做更完善的异常处理和推送。
 
## How to use

 First,Fork, set secrets [AIRPORTURL] [USERNAME] [USERPASSWD]   (Setting > Secrets > Actions)
 Then start Action, enable Workflow   (Project Main Page)
 Select checkin workflow, (Run Workflow > Run Workflow)
 If your secrets is right , the action will running successful.  
 And Multi URL split with &&.
 
 首先，您需要Fork , 并在Secrets中增加 [AIRPORTURL] [USERNAME] [USERPASSWD] 三个值。  (Setting > Secrets > Actions)
 最后点击Action，启用Workflow 。 （项目主页）
 点击 Run Workflow 运行。
 如果Secrets设置正确的值，脚本将会正常运行。
 支持多个机场签到，多个值使用&&分割。  


## Example

AIRPORTURL https://github.com

USERNAME LoginName

USERPASSWD LoginPassword

OR

AIRPORTURL https://github.com&&https://github.com

USERNAME LoginNameA&&LoginNameB

USERPASSWD LoginPasswordA&&LoginPasswordB

This use case shows that AIRPORTURL[0] USERNAME[0] USERPASSWD[0] these three attributes are a set of Web Login data.  
Note that the URL must be a string with HTTP (HTTPS), such as https://github.com , he must end with a domain name

此用例显示 AIRPORTURL[0] USERNAME[0] USERPASSWD[0] 这三个属性是一组Web登录数据。  
注意，URL必须是一个带Http（Https）的字符串，如https://github.com，他必须以域名结尾。  
## IMAGE
![image](https://user-images.githubusercontent.com/45820630/133551741-f836b3f8-b9f5-42c5-bb41-c09f4dcb7f59.png)


## Workflow Schedule POSIX Cron-style
[Github Workflow Document](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#onschedule)

The cron format consists of:  
```
*    *    *    *    *    *  
┬    ┬    ┬    ┬    ┬    ┬  
│    │    │    │    │    │  
│    │    │    │    │    └ day of week (0 - 6) (0 is Sun)  
│    │    │    │    └───── month (1 - 12)  
│    │    │    └────────── day of month (1 - 31)  
│    │    └─────────────── hour (0 - 23)  
│    └──────────────────── minute (0 - 59)  
└───────────────────────── second (0 - 59, OPTIONAL)  
```
