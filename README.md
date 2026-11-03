# FGODailyBonusLog

[FGODailyBonus](https://github.com/zhangbeihai9931/FGODailyBonus) 的签到日志仓库，由脚本自动读写。

## 目录结构

`
FGODailyBonusLog/
├── README.md          本说明
├── cfg.json           游戏版本配置（脚本自动维护，别手改）
└── YYYY/MM/DD.log     每天的签到结果
`

## 关于隐私

这个仓库是公开的，但**不包含任何账号凭证**：

- authKey / secretKey / userId 只存在 Actions Secrets 里，从不写入这里
- 日志里的玩家标识是**加盐 SHA-256 哈希**（16 位），无法反推
- 日志内容是游戏内统计：登录天数、等级、石头、呼符、体力、友情点

## 说明

- cfg.json 由脚本在发现版本过期时自动更新，不要手动改
- 同一天多次运行会覆盖同一个日志文件
- 日志可以随时删除，脚本只依赖 cfg.json
