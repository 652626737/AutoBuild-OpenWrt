# AutoBuild-OpenWrt
## 支持设备与编译状态：

点击下表中蓝色 “√” 即可跳转到该设备固件下载页面。

其中：

版本为 Lean 为基于 [Lean 大源码](https://github.com/coolsnowwolf/lede) 编译的固件 (Luci 采用 Lean 版 Luci 18.06 )；

版本为 Offical 为基于 [OpenWrt 官方源码](https://github.com/openwrt/openwrt/tree/master) Master 分支编译的固件 (Luci 采用官方版 Luci 19.07)；

版本为 Project 为基于 [Project-OpenWrt 源码](https://github.com/project-openwrt/openwrt/tree/18.06-kernel5.4) 18.06-kernel5.4 分支编译的固件，目前在仍处于测试阶段 (Luci 采用 Lean 版 Luci 18.06 )。

树莓派 2B 的固件通用于树莓派 2B、3B、3B+、4B，但板载无线功能可能不可用。

**请不要直接 Fork 此项目**，如果你想使用本项目编译 OpenWrt 固件，请前往：

<https://github.com/danxiaonuo/AutoBuild-OpenWrt>

在此项目的 [README.md](https://github.com/danxiaonuo/AutoBuild-OpenWrt/blob/master/README.md) 中有详细的使用教程~

## 注意事项：

1. 点击上表中蓝色 “√” 即可跳转到该设备固件下载页面。
2. 在固件编译完成后，会上传一份副本到 WeTransfer 和 奶牛快传，对于国内网络用户，为提高下载体验，可下载存放于这两个网站中的固件副本，副本下载地址在固件列表下的 Annotations 提示框内。在极少数情况下，因网络原因这两份副本可能会上传失败，如果遇到这种情况，就只能下载存放在 Github Action 里的固件了:
3. 由于 Github Action 限制，需要登录 Github 账号才可下载存放于 Github Action 中的固件 (未登录时固件链接不可被点击)，但 WeTransfer 和 奶牛快传 的固件下载链接在未登录状态下可正常查看，不受影响；
4. 如果需要下载存放于 Github Action 上的固件，由于众所周知的原因，请尽量使用科学上网方式下载固件，固件下载完成后，请下载 sha256sums 文件或使用压缩软件的 "测试压缩文件" 功能来验证固件的完整性；
5. 文件下载时默认被 zip 压缩，若有需要，请解压 zip 得到固件后再刷入；
6. 固件下载页面标注固件大小为解压 zip 文件后的大小，并非文件下载真实大小。例如，某文件在 Github Action 上标明的文件大小为 1.01G，但在下载过程中可能只会下载不到 300M 的一个 zip 压缩文件，解压后得到的文件大小才为标注的 1.01G；
7. 固件在每天凌晨 02:00 拉取 OpenWrt 源码和第三方软件包项目自动编译，默认情况下固件每日编译一次 (config 文件更新时除外)，未逐一经过实机测试，故不保证 100% 可靠性。
8. 固件 (功能性) 更新内容可前往 Telegram 频道: [Beautiful Apps Channel](https://t.me/beautifulapps) 查看。

## 文件说明:

除提供已编译好的固件外，本项目还提供以下文件:

1. 完整性校验文件: sha256sums
2. OpenWrt 编译配置: config.seed
3. 固件内已集成的软件包列表: openwrt-$target-$subtarget-$devices.manifest
4. OpenWrt 的软件包归档: packages.zip
5. 适用于 Windows / 集成 web 服务器的软件包归档 (便于搭建局域网软件包服务器): packages-server.zip

在 WeTransfer 和 奶牛快传 链接中，还提供以下文件:

1. OpenWrt Image Builder
2. OpenWrt SDK
3. OpenWrt Tool Chain

以上文件可按需下载。

## 鸣谢：

P3TERX/Actions-OpenWrt (本项目基于此项目):

<https://github.com/P3TERX/Actions-OpenWrt>

OpenWrt Source Repository:

<https://github.com/openwrt/openwrt/>

Lean's OpenWrt source:

<https://github.com/coolsnowwolf/lede>

CTCGFW's Team:

<https://github.com/project-openwrt>
