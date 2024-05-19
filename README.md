# scoop-autoremote

自用scoop的配置库。

使用gitlink的scoop安装，在powershell终端中执行。

```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
Invoke-RestMethod -Uri https://scoop.feynbin.cn | Invoke-Expression
```

gitlink的安装文件指向gitlink仓库，并且7zip从国内下载，默认配置githubproxy来加速github文件的传输。



scoop原版安装文件的加速版，在powershell终端中执行。

```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
Invoke-RestMethod -Uri https://scoop.pages.dev | Invoke-Expression
```

使用githubproxy加速scoop本体的下载和scoop-main仓库的下载。

如果已经安装git，那么会使用南京大学镜像站代理的scoop.git



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





