# 上应小风筝 Restful API

## 项目概要

本项目旨在为上海应用技术大学的学生提供校园信息整合与管理服务。

## 功能

- [x] 登录模块
- [x] 活动与签到
- [ ] 第二课堂
- [ ] 课表查询与选课
- [ ] 二手闲置交易
- [x] 入学信息查询
- [ ] 失物招领
- [ ] 每日学习打卡

## 项目设计

TODO: 项目设计文档。链接至 `docs/`

## 目标平台

阿里云 ECS（1G 1C） Debian 10

## 安装

请先确保系统中已预装有 rust 编程环境（rustc、cargo等），并已连接上互联网。

下载并编译：

```shell
git clone https://github.com/sunnysab/kite-server.git
cd kite-server
cargo build
```

同时修改根目录下 `kite.example.toml` 文件。默认如下：

```toml
# Server config
[server]
# HTTPS API service address.
bind = "0.0.0.0:443"
# Postgresql connection string.
db = "postgresql://user:password@address:port/database"
# Token secret for API.
secret = "secret"
# Directory path should be end with "\"
attachment = "D:\\tmp\\"

# Wechat platform config. Access https://mp.weixin.qq.com for details
[wechat]
# Miniprogram appid
appid = "111"
# Secret
secret = "111"

[host]
# Bind address, for accepting connections from agents
bind = "0.0.0.0:1040"
# Max agent connections
max = 32
```

微信相关接口（微信登录）需要填写 `appid` 和 `secret` 后才能使用。
执行下面命令即可运行，目标二进制文件存放在 `target` 目录下。

```shell
cargo run
```

## 有关项目

| 项目         | 说明             |
| ------------ | ---------------- |
| [kite-agent](https://github.com/sunnysab/kite-agent) | 后端数据抓取工具 |
| [kite-protocol](https://github.com/sunnysab/kite-protocol) | 通信协议库（已废弃）  |
| [kite-checking](https://github.com/snomiao/kite-checking) | 返校码管理后台（暂不使用） |
| [kite-admin](https://github.com/Crystal-RainSlide/kite-admin) | 综合管理后台（暂不更新） |


## 如何贡献

非常欢迎你的加入！[提一个 Issue](https://github.com/sunnysab/kite-server/issues/new) 或者提交一个 Pull Request。

如果您有意见或建议，可以联系我们。



## 开源协议

[GPL v3](https://github.com/sunnysab/kite-server/blob/master/LICENSE) © 上海应用技术大学易班 sunnysab

除此之外，您不能将本程序用于各类竞赛、毕业设计、论文等。