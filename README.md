### 树莓派 3B/3B+/4B OpenWrt 固件全自动编译 & 发布 Docker 镜像到 Dockerhub 

---

此项目参考 [SuLingGG/OpenWrt-Rpi](https://github.com/SuLingGG/OpenWrt-Rpi)，**在此表示感谢！**

本说明只包含此项目相关信息说明，包括但不限于：设备型号、源码版本、Docker镜像信息。

**关于固件及Docker镜像的详细使用说明请前往博客文章：**[树莓派 | Docker上运行 OpenWrt 做旁路由](https://blog.sillyson.com/archives/7.html)

*此博客将会持续更新关于树莓派与OpenWrt的相关文章，如果您觉得项目不错请持续关注哦~~*



#### 项目支持设备与编译状态：

---

| 固件类型        | 支持设备                              | 编译状态                                                     | 源码地址                                                     | 固件地址                                                     | Docker 镜像地址                                  |
| --------------- | ------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ |
| Lean            | 树莓派 3B/3B+/4B                      | ![](https://img.shields.io/github/workflow/status/1orz/My-action/Build-Lean-lede?label=) | [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)    | [Actions](https://github.com/scenerycm/OpenWrt-Raspi/actions) | [Dockerhub](https://hub.docker.com/repositories) |
| Offical-19.07   | 树莓派 3B/3B+<br />Docker镜像可用于4B | ![](https://img.shields.io/github/workflow/status/1orz/My-action/Build-Lean-lede?label=) | [openwrt/openwrt](https://github.com/openwrt/openwrt/tree/openwrt-19.07) | [Actions](https://github.com/scenerycm/OpenWrt-Raspi/actions) | [Dockerhub](https://hub.docker.com/repositories) |
| Project-OpenWrt | 树莓派 3B/3B+/4B                      | ![](https://img.shields.io/github/workflow/status/1orz/My-action/Build-Lean-lede?label=) | [project-openwrt/openwrt](https://github.com/project-openwrt/openwrt/tree/18.06-kernel5.4) | [Actions](https://github.com/scenerycm/OpenWrt-Raspi/actions) | [Dockerhub](https://hub.docker.com/repositories) |

固件说明：

- Lean 版固件基于 Lean 大源码编译 (Luci 采用 Lean 版 Luci 18.06 )
- Offical-19.07 版固件基于 OpenWrt 官方 19.07 源码编译
- Project-OpenWrt 版固件基于 Project-OpenWrt 源码18.06-kernel5.4 分支编译，基于此固件的 Docker 镜像也是我一直在 3B+ 上使用的固件，**较为推荐**。

- 其中基于各类固件的 Doker 镜像在树莓派 3B、3B+、4B 上通用。

**下载固件与 Docker 镜像请点击表格中相应的栏位。**

- Actions 提供编译好的所有固件与软件包、完整性校验文件、OpenWrt 编译配置等。
- Dockerhub 提供基于每日编译的固件制作的最新版 Docker 镜像，同时也提供历史版本镜像下载。

**注意**：由于国内到 github 与 dockerhub 的网络偶尔会抽风，建议在良好的网络环境下下载相关文件。



#### 使用 Docker 运行 OpenWrt 的优势

---

这里多说两句，为什么要提供 Docker 镜像？

本人之前在树莓派 3 上用了一段时间发现 Open­Wrt 对资源的消耗还是很低的，毕竟我的带宽只有 100M，而且树莓派的硬件性能相比传统的路由器还是高了很多。如果让 Open­Wrt 运行在 dokcer 里将其与底层 linux 系统解耦，不仅可以利用树莓派的剩余性能去做一些其他的事情，对于 Open­Wrt 的备份及迁移来说也更方便。

**更重要的一点是，我们可以同时让多个版本的 Open­Wrt 运行在 dokcer 中，可以同时完成对多个固件的测试工作。时间就是生命啊!**



#### 感谢

---

- [SuLingGG/OpenWrt-Rpi（非常感谢）](https://github.com/SuLingGG/OpenWrt-Rpi)

- [OpenWrt Source Repository](https://github.com/openwrt/openwrt/)

- [Lean's OpenWrt source](https://github.com/coolsnowwolf/lede)

- [CTCGFW's Team](https://github.com/project-openwrt)