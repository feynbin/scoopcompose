# scoop-autoremote

自用scoop的配置库。

将scoop代码库以及scoop官方推荐的几个bucket搬运到gitlink。用于优化scoop的使用

使用gitlink的scoop安装，在powershell终端中执行。

```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
Invoke-RestMethod -Uri https://scoop.feynbin.cn | Invoke-Expression
```

---

### 高级安装

使用以下命令获取安装脚本

```
irm scoop.feynbin.cn -outfile install.ps1
```

使用以下命令将scoop安装到指定位置

```
.\install.ps1 -ScoopDir 'D:\Scoop' -ScoopGlobalDir 'D:\ScoopGlobalDir' -NoProxy | Out-Null
```

安装完成后，如果你没有安装git和7zip，你还需要安装这两个工具用于scoop的使用。

使用`scoop.feynbin.cn`安装的scoop，获取到的本地main仓库中，7zip以及git安装地址被修改为南京大学镜像站地址。因此国内使用可以直接安装。



---

如果你不喜欢我这样的配置，或者觉得麻烦，我在原版scoop安装的基础上，配置了githubproxy来进行加速，使用的是GitHubProxy的教程搭建的地址。对比`mirror.ghproxy.com`，多了ipv6连接，对于校园网环境较为友好。

---

scoop安装的GitHubProxy版本，在powershell终端中执行。

```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
Invoke-RestMethod -Uri https://scoop.pages.dev | Invoke-Expression
```

注意，如果已经安装git，那么会使用南京大学镜像站代理的scoop.git

高级安装同上，将地址改为`scoop.pages.dev`即可。

搬运了scoop官方推荐的bucket库到国内。每天更新两次。添加使用以下命令。

```
scoop bucket add main https://gitlink.org.cn/feynbin/Main
scoop bucket add extras https://gitlink.org.cn/feynbin/Extras
scoop bucket add versions https://gitlink.org.cn/feynbin/Versions
scoop bucket add java https://gitlink.org.cn/feynbin/Java
scoop bucket add nirsoft https://gitlink.org.cn/feynbin/Nirsoft
scoop bucket add nonportable https://gitlink.org.cn/feynbin/Nonportable
scoop bucket add php https://gitlink.org.cn/feynbin/Php
```





