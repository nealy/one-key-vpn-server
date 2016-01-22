# one-key-vpn-server

一键搭建 IPSec IKEv2 VPN 服务器，适用于 CentOS 6.x 和 Ubuntu

## 使用方法

#### 下载脚本到服务器

```bash
wget https://raw.githubusercontent.com/nealyg/one-key-vpn-server/master/one_key_setup_IPSEC_IKEV2_VPN.sh
```

#### 以管理员身份运行

```bash
chmod +x one_key_setup_IPSEC_IKEV2_VPN.sh #赋予脚本执行权限
bash one-key-ikev2.sh
```
支持使用自己的私钥和根证书，如果有需要，请在运行脚本之前将私钥命名为ca.pem、根证书命名为ca.cert.pem，放到脚本所在目录。    
脚本执行过程中，根据提示输入相关设置并回传即可。

> Tips:    
> 脚本会提示选择VPS主机架构（OpenVZ还是Xen、KVM），如果是普通服务器，选1即可，如果是VPS主机必须正确选择架构才能正常安装。    
> 脚本完成后会显示默认设置的用户名/密码，可根据提示自行修改。    
> 服务器若重启，需要重新启动ipsec: `ipsec start`    
> 更多详细信息请参阅 [在CentOS/Ubuntu下搭建 IPSec/IKEv2 VPN](www.mynook.xyz/2016/setup-vpn-server-on-centos-by-strongswan/)
