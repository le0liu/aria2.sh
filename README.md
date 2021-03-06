# Aria2 一键安装管理脚本
[![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square)](https://github.com/P3TERX/aria2.sh/blob/master/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/P3TERX/aria2.sh.svg?style=flat-square&label=Stars)](https://github.com/P3TERX/aria2.sh/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/P3TERX/aria2.sh.svg?style=flat-square&label=Fork)](https://github.com/P3TERX/aria2.sh/fork)

## 系统要求
CentOS 6+ / Debian 6+ / Ubuntu 14.04+

## 下载安装
执行下面的代码下载并运行脚本，出现脚本操作菜单输入 `1` 开始安装。
```
wget -N https://raw.githubusercontent.com/P3TERX/aria2.sh/master/aria2.sh && chmod +x aria2.sh && bash aria2.sh
```
## 使用说明
进入下载脚本的目录并运行脚本，然后选择你要执行的选项即可。
```
./aria2.sh
```

## 其他操作
启动：`/etc/init.d/aria2 start`

停止：`/etc/init.d/aria2 stop`

重启：`/etc/init.d/aria2 restart`

查看状态：`/etc/init.d/aria2 status`

配置文件：`/root/.aria2/aria2.conf` （配置文件包含中文注释，但是一些系统可能不支持显示中文）

令牌密匙：随机生成（可以自己修改 7. 修改 配置文件）

默认下载目录：`/root/Download`

## 附加功能
整合了 [Aria2 完美配置](https://github.com/P3TERX/aria2_perfect_config)，包含如下附加功能脚本：

`delete.aria2.sh` 下载完成后删除 .aria2 文件。

`delete.sh` 下载错误和停止后删除文件（包括 .aria2 文件），避免占用空间。

`autoupload.sh` 下载完成后自动调用 rclone 上传(move)到网盘，删除 .aria2 文件，过滤无用文件等。（可选，[使用教程](https://p3terx.com/archives/offline-download-of-onedrive-gdrive.html)）

## 更新日志
### 2018-12-8 v2.0.2
* 修复 配置脚本没有执行权限的bug

### 2018-12-7 v2.0.1
* 修复 设置下载文件夹提示不存在的 bug
* 解锁 更新 BT-Tracker服务器 选项

### 2018-12-7 v2.0.0α
* 整合 [Aria2 完美配置](https://github.com/P3TERX/aria2_perfect_config)

### 2018-10-18 v1.1.10
* 取自[一个逗比写的逗比脚本](https://github.com/P3TERX/doubi_backup)
* 感谢 Toyo 大佬
