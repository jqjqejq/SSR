# 梅林固件的科学上网插件安装
1.首先在koolshare论坛下载最新的梅林固件<br>
  https://www.koolcenter.com/posts/36<br><br>
2.将下载好的梅林固件刷入到路由器，刷入教程网上有很简单
  （要附有挂载虚拟内存的教程，准备个2G的U盘）<br><br>
3.刷好固件后会在最下方多出个【软件中心】，点击进入，将软件中心更新到最新版本，<br>
  然后点击【未安装】的tab标签，找到【科学上网】插件，点击安装。<br>
  等待安装完成会在【已安装】tab标签内显示，图标是熟悉的小飞机。<br>
  点击小飞机图标进入插件配置界面，插件简介如下：<br>
  (本插件是支持SS、SSR、KoolGame、V2Ray四种客户端的科学上网、游戏加速工具。)
  
# 插件简单介绍
<strong>1.【账号设置】-填写账号信息-【保存&应用】-即可科学上网</strong><br>
  这里有一个【模式】的选择，一般正常浏览网站看视频等个人认为选择gfwlist模式（即分流模式-国内网站不走SSR/SS）即可。<br>
  【1】gfwlist模式:<br>
    该模式使用gfwlist区分流量，Shadowsocks会将所有访问gfwlist内域名的TCP链接转发到Shadowsocks服务器，实现透明代理；<br>
    和真正的gfwlist模式相比较，路由器内的gfwlist模式还是有一定缺点，因为它没法做到像gfwlist PAC文件一样，对某些域名的二级域名有例外规则。<br>
优点：节省SS流量，可防止迅雷和PT流量。<br>
缺点：代理受限于名单内的4000多个被墙网站，需要维护黑名单。一些不走域名解析的应用，比如telegram，需要单独添加IP/CIDR黑名单。<br>
【2】大陆白名单模式:<br>
    该模式使用chnroute IP网段区分国内外流量，ss-redir将流量转发到Shadowsocks服务器，实现透明代理；<br>
    由于采用了预先定义的ip地址块(chnroute)，所以DNS解析就非常重要，如果一个国内有的网站被解析到了国外地址，那么这个国内网站是会走ss的；<br>
    因为使用了大量的cdn名单，能够保证常用的国内网站都获得国内的解析结果，但是即使如此还是不能完全保证国内的一些网站解析到国内地址，这个时候就推荐使用具备cdn解析能力的cdns或者chinadns2。<br>
优点：所有被墙国外网站均能通过代理访问，无需维护域名黑名单；主机玩家用此模式可以实现TCP代理UDP国内直连。<br>
缺点：消耗更多的Shadowsocks流量，迅雷下载和BT可能消耗SS流量。<br>
【3】游戏模式:<br>
    游戏模式较于其它模式最大的特点就是支持UDP代理，能让游戏的UDP链接走SS，主机玩家用此模式可以实现TCP+UDP走SS代理；<br>
    由于采用了预先定义的ip地址块(chnroute)，所以DNS解析就非常重要，如果一个国内有的网站被解析到了国外地址，那么这个国内网站是会走ss的。<br>
优点：除了具有大陆白名单模式的优点外，还能代理UDP链接，并且实现主机游戏 NAT2!<br>
缺点：由于UDP链接也走SS，而迅雷等BT下载多为UDP链接，如果下载资源的P2P链接中有国外链接，这部分流量就会走SS！<br>
【4】全局模式:<br>
    除局域网和ss服务器等流量不走代理，其它都走代理(udp不走)，高级设置中提供了对代理协议的选择。<br>
优点：简单暴力，全部出国；可选仅web浏览走ss，还是全部tcp代理走ss，因为不需要区分国内外流量，因此性能最好。<br>
缺点：国内网站全部走ss，迅雷下载和BT全部走SS流量。<br>
【5】回国模式:<br>
    提供给国外的朋友，通过在中间服务器翻回来，以享受一些视频、音乐等网络服务。<br>
提示：回国模式选择外国DNS只能使用直连~

<strong>2.【节点管理】-登录的节点会在此处显示。<br><br>
3.【故障转移】-当一个节点不能联网时会自动换下一个节点尝试联网。<br><br>
4.【DNS设定】-选择适合的DNS即可，如果不能联网，多试几个DNS。<br><br>
5.【黑白名单】-设定走不走代理。<br><br>
6.【KCP加速】-首先确保当前节点支持KCP加速。开启之后浏览国外网站会快一些，甚至节点好的可以看4K视频。有兴趣网上搜索教程。<br><br>
7.【UDP加速】-游戏加速，网页打开速度加快。<br>
  https://github.com/wangyu-/UDPspeeder/blob/master/doc/README.zh-cn.v1.md<br><br>
8.【更新管理】-这里填写你需要订阅的节点。<br>
  将订阅的节点填入【SSR/v2ray订阅设置】-【订阅地址管理（支持SSR/v2ray）】内，选好模式、自动更新时间，然后点击【保存并订阅】即可。
</strong>

# 免费机场
1.附上几个免费机场：<br><br>
  【桔子云】老牌机场。（记得每日签到获取更多流量）<br>
  https://juzi69.com/auth/register?code=8aN6<br><br>

免费机场<br><br>
https://raw.githubusercontent.com/ssrsub/ssr/master/ssrsub<br><br>
https://qiaomenzhuanfx.netlify.com/<br><br>
https://muma16fx.netlify.com/<br><br>
https://raw.githubusercontent.com/voken100g/AutoSSR/master/online<br><br>
https://raw.githubusercontent.com/voken100g/AutoSSR/master/recent<br><br>
