# Markdown图床

Markdown作为一种纯文本格式的标记语言，通过简单的标记语法，就使普通文本内容具有一定的格式。一次标记可以做到各平台通用，免除了富文本编辑器换平台就要重新排版的繁琐，越来越受欢迎，尤其是程序员群体。现在很多论坛和社区都开始支持使用Markdown。但使用markdown也有一个重要的问题，那就是图片的存储，markdown文件要用到图片时必须是一个链接。各个平台都有自己的图片存储方法，在不使用图床的情况下，同一篇文章发布到不同的平台需要单独上传图片一次。这个真的无法接受，太麻烦。

解决办法就是使用图床来单独存储图片，需要用到图片的地方统一用图床上的图片链接就好了。这样同一篇文章，发布到不同的平台真正可以简单复制粘贴。

图床就是一个图片服务器，用来存储图片，以URL的形式来供其他平台获取图片。可以自己搭建，也可以使用别人搭建好后提供的服务。自己搭建肯定花钱，别人搭建给你提供服务，有的收费，有的一定范围内不收费，有的完全免费。

> 重要提示：数据是比金钱更重要的东西！这点务必先搞清楚。不要因为追求免费而用可能损失数据的服务，这样以后会发现，特别不值。即丢失了数据，又重新花钱，还浪费了时间。

一般选择图床要满足下面条件

- `可靠性`。数据在当今社会是最宝贵的财富之一，因此在选择存储的服务时，可靠性无疑是首要的考虑因素。
- `安全性`。面对攻击、盗取和破坏时如何保障数据不受到损失，是另一个重要的考虑因素。
- `是否简单易用`。越简单易用越好。
- `价格是否合理`。在满足前两条的情况下，越便宜越好，最好免费。

把网上搜集到的能作为图床的方法总结了一下（后附我的选择方案）

网上类似文章

- [盘点一下免费好用的图床-知乎](https://links.jianshu.com/go?to=https%3A%2F%2Fzhuanlan.zhihu.com%2Fp%2F35270383%3Fivk_sa%3D1023345p)
- [分享8个高速稳定的图床网站-简书](https://www.jianshu.com/p/c35091dcba84)

## 搜集到的作为图床的方法

- 对象存储图床
  - 国外的有amazon s3 和google storage等
  - 国内的有七牛云、又拍云、腾讯云、阿里云、天翼云等
- 第三方图床
  - sm.ms、imgchr、聚合图床等
- 云盘图床
  - 微云等
- 社交网站图床
  - 新浪微博、qq空间等
- 云笔记图床
  - 印象笔记、有道云笔记等
- 代码托管网站图床
  - github、码云等
- 自建图床
  - github开源图片服务Cheverto
- 区块链存储图床
  - IPFS等

### 对象存储图床

关于什么对象存储，请参考[什么是对象存储？](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.getnas.com%2Fwhat-is-oss%2F)。很多大公司都提供对象存储的服务，可以作为图床来使用。国外的有amazon s3 和google storage等；国内的有七牛云、又拍云、腾讯云、阿里云、天翼云等。网上对于这些服务的对比可以看一看：[8个免费对象存储空间云存储服务对比及选择建议](https://links.jianshu.com/go?to=https%3A%2F%2Fchonzi.com%2F8816.html)

#### 七牛云对象存储

注册认证后有10G永久免费空间，每月10G国内和10G国外流量，速度相当快，无图片上传限制。七牛云是国内专业CDN服务商，插件支持比较多，有免费ssl证书。

- [七牛云官网-对象存储](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.qiniu.com%2Fproducts%2Fkodo)
- [七牛云官方文档-对象存储-快速入门](https://links.jianshu.com/go?to=https%3A%2F%2Fdeveloper.qiniu.com%2Fkodo%2Fmanual%2F1233%2Fconsole-quickstart)
- [七牛云对象存储价格](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.qiniu.com%2Fprices%3Fsource%3Dkodo)（标准存储，低至 0.099 元/GB/月起）

特别注意：

1. 七牛云30天后会回收测试域名，因此你必须要绑定自己的已经备案的域名。也就是说，要想用这个免费服务，首先你必须花钱购买域名和服务器，并且备案。只要一个域名为什么还要买服务器呢？因为这是管局的规定，域名备案是必须有服务器的，因为域名是一个独立的个体，属于网站的一部分，另外一部分网站的程序还需要放在服务器上，才算是完成网站的搭建。服务器和域名每年都需要续费，所以，虽然七牛云提供10G免费的空间，但这并不是一个免费的方案。如果你决定用，具体步骤可参考：1、[在七牛云官网开通存储空间](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.qiniu.com%2Fproducts%2Fkodo) 2、[购买域名并备案](https://links.jianshu.com/go?to=https%3A%2F%2Fjingyan.baidu.com%2Farticle%2Ffc07f9896d741512ffe519d9.html) 3、[七牛云外链绑定自己域名](https://links.jianshu.com/go?to=https%3A%2F%2Fblog.csdn.net%2Fweixin_38187317%2Farticle%2Fdetails%2F83987258)
2. https流量收费。即如果图片链接想用https，那么必须升级，收费。

#### 又拍云对象存储

注册认证后有10G永久免费空间，每月15G的HTTP和HTTPS流量，无图片上传限制，提供两款可以免费续期的SSL证书。

- [又拍云官网-对象存储](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.upyun.com%2Fproducts%2Ffile-storage)
- [又拍云联盟](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.upyun.com%2Fleague)
- [又拍云服务价格计算器](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.upyun.com%2Fpricing)（日存储容量 ≤ 日CDN流量时免费；
  存储容量 ＞ 日CDN流量时。超过部分日存储容量 0.0043 元/GB/日、0.129 元/GB/30天)

特别注意：

1. 需要绑定自己的已备案域名。同七牛云
2. 又拍云认证比较麻烦
3. 需要加入又拍云联盟计划才可享受以上待遇。（在网站底部添加又拍云logo及官网链接）

#### 腾讯云对象存储

仅六个月的免费存储容量、免费请求和免费流量。

- [腾讯云官网-对象存储](https://links.jianshu.com/go?to=https%3A%2F%2Fcloud.tencent.com%2Fproduct%2Fcos)
- [腾讯云官方文档：对象存储 COS](https://links.jianshu.com/go?to=https%3A%2F%2Fcloud.tencent.com%2Fdocument%2Fproduct%2F436)
- [腾讯云对象存储价格](https://links.jianshu.com/go?to=https%3A%2F%2Fbuy.cloud.tencent.com%2Fprice%2Fcos%23E4B8ADE59BBDE5A4A7E99986E59CB0E59F9FE5AE9AE4BBB7)

对象存储 COS 的计费项包括：存储容量费用、请求费用、数据取回费用、流量费用、和 管理功能费用。听着就头大

#### 阿里云对象存储

貌似没有免费额度。

- [阿里云官网-对象存储](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.aliyun.com%2Fproduct%2Foss%3Fspm%3D5176.12825654.h2v3icoap.37.3dbd2c4aXVI5bn%26aly_as%3DMYomFRkR)
- [阿里云官方文档：对象存储 OSS](https://links.jianshu.com/go?to=https%3A%2F%2Fhelp.aliyun.com%2Fproduct%2F31815.html%3Fspm%3Da2c4g.11186623.6.540.19ac1c629mGAaM)
- [阿里云对象存储价格](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.aliyun.com%2Fprice%2Fproduct%3Fspm%3D5176.7933691.1309819.7.26ec2a66QzlDFd%26aly_as%3Dydeh02mJ%23%2Foss%2Fdetail)

对象存储 OSS 的计费项包括：存储费用、流量费用、请求费用、数据处理费用、对象标签费用、传输加速费用。跟腾讯云一样头大。

### 第三方图床

第三方图床就是专门做图床的服务商，常见的有 sm.ms、imgchr、聚合图床等

#### sm.ms

免费版存储容量5GB，每分钟限制上传20张，每小时限制上传100张，每天限制上传200张，每周限制上传500张，每月限制上传1000张，单张图片最大5M。不支持相册，找图片需要用搜索功能

- [sm.ms官网](https://links.jianshu.com/go?to=https%3A%2F%2Fsm.ms%2F)
- [做了一个图床网站 sm.ms](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.v2ex.com%2Ft%2F182703)（sm.ms作者在V2EX上的帖子）

#### imgchr

免费版存储容量不限，每小时限制上传30张，每天限制上传次数为120次，单张图片最大10M。支持相册。仅限于非商用。

- [imgchr官网](https://links.jianshu.com/go?to=https%3A%2F%2Fimgchr.com%2F)(中文名为路过图床)

#### 聚合图床

将图片分发到多处备份，借助其本身的CDN加速功能，节省服务器流量，并且不用担心图片被删除，即便其中某几个图床上的图片被删除了，还有其他备份，保证万无一失，支持匿名和注册管理

免费版无API支持，跳转链接无法保证永久有效，若链接失效需要您重新上传获取新链接。最多存1000张，单张图片大小5M，不支持相册。

- [聚合图床官网](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.superbed.cn)

### 云盘图床

云盘一般都是文件系统存储，传图片获得外链即可。

- 微云：[利用微云来做你的图床](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.aihoom.com%2F599.html)

试了下百度网盘，分享图片可以生成永久链接，但必须要有提取码，肯定不合适做图床了。其他的没试，可以自行测试使用

### 社交网站图床

社交网站也能发图片，相应的也就可以获得图片的外链。其中用的比较多的是微博图床和qq空间图床。

- 新浪微博：[新浪图床怎么用](https://links.jianshu.com/go?to=https%3A%2F%2Fjingyan.baidu.com%2Farticle%2F46650658feb199f549e5f8fb.html)、[可以把新浪微博作为图床使用吗？](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.zhihu.com%2Fquestion%2F19876644%3Fsort%3Dcreated)
- qq空间：[图床使用QQ空间会出现问题吗？](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.zhihu.com%2Fquestion%2F37688721)

特别注意：微博图床一直以来是大家喜欢的免费好用的图床。但2019年4月25日，微博开启了图片防盗链，Referrer不为空且不是新浪的站点，全部返回403错误，也就是说非新浪的站点无法引用新浪服务器里的图片了。目前可以通过修改referrer的属性来绕过这个限制，但不保证新浪不会采取进一步的措施，毕竟用的人多了，服务成本太大，公司也承受不住。这种方法已经不再安全。

### 云笔记图床

云笔记同样也可以传图片，获取外链。比较出名的有印象笔记、有道云笔记。

- 印象笔记：[使用印象笔记作为图床](https://links.jianshu.com/go?to=https%3A%2F%2Fzhuanlan.zhihu.com%2Fp%2F73283533)
- 有道云笔记：[使用有道云笔记作为图床](https://links.jianshu.com/go?to=https%3A%2F%2Fbaijiahao.baidu.com%2Fs%3Fid%3D1632687069476377425%26wfr%3Dspider%26for%3Dpc)

### 代码托管网站图床

常用的代码托管网站有github、gitlab、码云、coding等，这些网站也可以上传图片，网站生成的外链就可以用在markdown中。

主要有三种方法：新建一个仓库，专门放图片、使用pages服务、使用issues功能。

- [新建github仓库（GitHub repo）做图床](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.cnblogs.com%2Fly-2019%2Fp%2F11828790.html)
- [github的issues功能做图床](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.cnblogs.com%2Fnull-%2Fp%2F10051036.html)
- [利用码云的 Gitee Pages 服务搭建个人图床](https://links.jianshu.com/go?to=https%3A%2F%2Fcloud.tencent.com%2Fdeveloper%2Farticle%2F1550782)

### 自建图床

自建图片服务器，顾名思义就是自己花钱购买服务器来搭建用来存储图片的服务。github有一个开源的图片服务Cheverto，可以用来搭建自己的图床。

- [Cheverto官网](https://links.jianshu.com/go?to=https%3A%2F%2Fchevereto.com%2Ffree)
- [Cheverto的github地址](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2FChevereto%2FChevereto-Free)
- [使用Cheverto搭建一个自己的图床网站](https://www.jianshu.com/p/7863fcb34aed)（此文章用到了docker，你需要懂docker）

自建图床非程序员玩不转，租服务器贵不说，关键是麻烦，还要去维护。就算搞好了，万一以后不想维护了呢？再说了，租服务器也不少花钱，为什么不直接购买大厂的服务呢？当然你要有能力有实力有别的业务也用服务器，当我没说，这里只是想找个图床用而已。

### 区块链存储图床

如果了解区块链，就会知道IPFS，它的远景很大，其中一个功能就是存储，我们也可以用它来作为图床。将是一种全新的体验，不过目前来看，尚早。持续关注中...

## 我的选择

对象存储里七牛云和又拍云都需要备案域名，还是要花域名和服务器的钱，不划算。腾讯云和阿里云收费项繁多，看不懂，个人用也有点浪费。

第三方图床最担心的是不稳定，不知道哪一天服务商就关门大吉了。极简图床的就是个例子。经过时间考验有成熟商业模式的可以考虑。

云盘图床、社交网站图床、云笔记图床最担心的是做限制，不知道哪一天这些网站就对外链做限制了。微博图床就是个例子。

自建图床难度系数太高，费时费力。

区块链新型图床尚早，看未来吧。

代码托管网站本身比较稳定安全，可以用来存放个人少量图片。

基于以上分析，我的图床选择是

- 常用：[利用码云仓库作为图床](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.cnblogs.com%2Fimist%2Fp%2F11417582.html)
- 备用：[sm.ms图床](https://links.jianshu.com/go?to=https%3A%2F%2Fsm.ms%2F)、[imgchr图床](https://links.jianshu.com/go?to=https%3A%2F%2Fimgchr.com%2F)(路过图床)
- 备份：github、百度网盘

之所以选择gitee而没选择github是因为国内访问速度有时候不是很快，影响体验。第三方图床作为备用图床，可以放一些不太重要的图片。github和百度网盘可以作图片的备份，防止数据丢失。

## 压缩图片

上传图片之前建议压缩一下，可以减少空间使用，并有效加快图片载入速度。比较好的压缩工具如下

- [TinyPNG官网](https://links.jianshu.com/go?to=https%3A%2F%2Ftinypng.com)

## 图床管理工具

选择好图床后肯定就是上传并使用图片了，这时就会面对一个问题，那就是每次都要去图床上传，然后复制链接，然后回到使用图片的平台粘贴使用。特别麻烦。所以就出现了图床管理工具帮助我们快速上传图片并获取图片URL链接。这样就省去了自己操作的繁琐。

以下是一些优秀的图床管理工具

- [PicGo官网](https://links.jianshu.com/go?to=https%3A%2F%2Fmolunerfinn.com%2FPicGo%2F)、[PicGo-github地址](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2FMolunerfinn%2FPicGo)(windows系统、mac系统)
- [VScode-PicGo插件](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2FPicGo%2Fvs-picgo)
- [MPic官网](https://links.jianshu.com/go?to=http%3A%2F%2Fmpic.lzhaofu.cn)、[MPic官网](https://links.jianshu.com/go?to=http%3A%2F%2Fmpic.lzhaofu.cn)（windows系统）
- [shareX官网](https://links.jianshu.com/go?to=https%3A%2F%2Fgetsharex.com%2F)、[shareX-github地址](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2FShareX%2FShareX)(windows系统)
- [uPic官网](https://links.jianshu.com/go?to=https%3A%2F%2Fblog.svend.cc%2Fupic)、[uPic-github地址](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2Fgee1k%2FuPic)（mac系统）
- [PicUploader官网](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.xiebruce.top%2F17.html)、[PicUploader-github地址](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2Fxiebruce%2FPicUploader)(windows系统、mac系统)

PicGo很好，但对码云不太好。我是mac系统，所以用的uPic，官网有详细的使用手册，支持 smms、 又拍云 USS、七牛云 KODO、 阿里云 OSS、 腾讯云 COS、微博、Github、 Gitee、 Amazon S3、自定义上传接口。而且还可以选择上传前压缩图片。压缩工具都省了。

需要注意：

1. 图床设置里面注意path的选择，这个就相当于一个相册，如果想把图片存到别的相册就要修改path路径。
2. 这种方法添加一张图片就要上传一次到码云，会产生很多的提交记录。个人用图片量不大时可以，图片量大的话会有滥用码云的可能，官方可能会采取一些措施。





> 作者：高鸿祥
> 链接：https://www.jianshu.com/p/ea1eb11db63f