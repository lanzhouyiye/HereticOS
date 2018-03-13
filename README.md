# 异数OS（HereticOS）  
  
## 简介  
  
异数OS是一种高性能海量并发操作系统，提供每CPU核80M每秒的线程切换能力，40M的event生成以及io能力，目前实做的TCP协议栈可达到每CPU核20M的io能力，并发容量相比传统操作系统提升1000倍，IO性能提升100倍。
  
### 短链接性能
  
|异数OS TCP单核短链接	|Seastar-Httpd长链接	|F-Stack nginx 短链接| F-Stack nginx 长链接|	Asio epoll长连接|	Asio epoll短链接| 
| :-------- | --------|  --------|--------| --------|--------:|  
|400W 	|70W|	9W |20W|14W（不可多核扩充）|	4W（不可多核扩充）|  

    
### 长连接性能  

|对比项目	|异数OS 2018|异数OS 2015+Win7|异数OS 2015+Win10	|360push|Whatsapp |  
| :-------- | --------|  --------|--------| -------- |--------:|  
|CPU占用数量	|1 	|16|	16|	24|	12|  
|内存占用	|4G	|64G	|64G	|256G	|128G|  
|实现的链接数	|1200W	|1000W|	300W	|100W	|300W|  
|使用的技术平台	|寄宿Linux下+异数自主协议栈	|寄宿win下+iocp	|寄宿win下+iocp	|Go+epoll	|Erlang+epoll  |  
|测试内容	|ECHO |推拉	|仅推	|仅推	|仅推	|仅推|  
|推送性能	|4.5M	|12W	|40W	|2W	|12W|  
|折算的IO性能|	9M	|12W	|40W	|2W	|12W|  
|已知问题	|缺乏经费支持|	缺乏经费支持|	缺乏经费支持|	容易宕机，要反复重启|	特制应用平台，不通用。|  
  
  
## 合作开发授权协议  

为了异数OS以及合作伙伴的顺利发展  
目前将异数OS合作伙伴授权目前分下列五类  
  
  

## 1. 友情合作者授权
给予异数OS经费捐赠，基金支持或者技术咨询，共同开发合作的个人或者单位，将获得友情合作者授权证书，异数OS将免费提供非保密的技术咨询，以及相关活动支援，并在所有授权协议证书官方网站的重要位置标明友情合作者信息。    
  

目前获得友情合作者授权的单位有：   
1.飞腾服务器平台提供商   
江苏先安科技有限公司 www.syan.com.cn
   
   
   
## 2. 普通开发者授权协议
普通开发者申请并移植开发一些应用产品到异数OS平台后获得异数OS普通开发者证书，开发者可使用异数OS开发者证书在一些需要异数OS产品开发的公司寻找职业发展机会，开发者免费提供给异数OS商业内容无关的源代码并允许异数OS免费自由使用并商业出售，商业出售开发者可获得5%的软件销售收入作为研发提成，如果有参加销售活动并签订软件销售合同，则可再增加5%的销售提成，普通开发者授权协议在开发者停止软件源代码维护时终止授权，并由异数OS托管相关权利和利益。

## 3. 基金支援者授权  
由于异数OS开发者经费不足，不利于异数OS的持续开发，所以开放此授权鼓励有信仰的支持国产操作系统的同学在经济上来给予异数OS帮助，捐助属于有偿捐助，并且可自愿退出取回捐助，异数OS并不真正使用和花费这些捐助，异数OS会使用这些钱用于购买一些本金安全的T+1基金产品比如货币基金，通过得到的利息来供应异数OS的开发活动，异数OS未来如果有产品销售收入，将会拿出相关利润用于基金捐助者分红，初期基金规模1亿，拿出50%的产品销售收入用于分红。

## 4. 创业开发者授权协议
创业开发者需要与异数OS沟通签订创业合作协议来得到创业开发者授权，得到创业开发者授权的用户可在创业目标领域得到一定协议时间的必要的竞争保护，异数OS将停止创业者目标领域的其他用户授权，已授权的用户将停止更新维护，创业合作者如果有使用其他普通开发者授权软件时，需要考虑支付或者收买普通开发者授权。  
  
  

## 5. 异数OS买断者
买断者与异数OS达成买断意向后，得到异数OS 源代码，买断者需要延续已经获得的普通开发者授权和创业开发者授权，买断者需要自行理清收回已获得的普通开发者授权和和创业开发者授权。  
  
## Q：异数OS与linux windows的关系
为了方便异数OS生态建设，目前异数OS寄宿在linux windows下，与他们共生，提供他们不能提供的海量并发任务调度，惰性IO管理等能力。  

## Q：异数OS为何不开放源代码
A：为了保护开发者利益，异数OS源代码不开放给任何人，除非买断，因为世界上能用异数OS的用户可以用10个指头数过来，如果开源，对开发者来讲就没有任何谈判意义，异数OS开发者需要像销售一样向你的老板谈判血汗的价值，源代码只有异数OS买断者可以获得。  

## Q：开发合作是否提供SDK  
A: 由于异数OS采用大量静态编译优化技术，且需要联合考虑应用实际负载情况作出相关定制调整，所以需要开发者提供源代码，进行联合编译优化，后面会提供给开发者假接口用于编译调试，实施具体项目时，整理出项目实际需求(容量性能硬件环境)以及项目源代码提交给异数OS,由异数OS调整相关参数联合编译出项目需要的二进制版本。

## 技术社区
QQ群 652455784
