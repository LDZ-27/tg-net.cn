# tg-net.cn
深圳市万网博通科技有限公司多业务智能管理系统未授权访问漏洞详情



可以获取内网设备信息，以及重置系统导致无法正常使用，可以更改ap配置使攻击者近源接入内网等等，重启指定路由器等等
exp包含获取内网热点，dos设备

默认口令
ap信息
详细ap信息
关闭arp防护
恢复出厂设置（多数情况就是dos了）
dns劫持内网（需要指定代理ip，掩码，网关，主dns备用dns）
因为获取这些数据需要登录，修改不需要，鸡肋

检测是否存在未授权访问的poc目前正在提交goby
危害较大的poc比如能够导致系统重置网络瘫痪的，交换机（未测试）和业务管理系统的重置系统将保存在这个仓库
其余的poc默认口令，ap信息，默认密码热点（admin），关闭arp防护等都保存在这个仓库保存

用法统一为 ./exp脚本.sh ip:端口

goby的poc不包含exp，原因是该漏洞无法获取系统权限，并且存在dos的可能，对业务危害大，所以就不去花时间写goby poc导致可能的滥用了
该漏洞最早发现时间是 2023 1月 22日晚，因为危害可能不大没有重视，和群友门吹逼的day红包。
请勿用于未经授权的渗透测试
by lvdouzhou
