# 💻 蔚蓝档案命令手册
**📝 作者：[AzureXuanVerse](https://github.com/AzureXuanVerse)**

> 🎮 适用于 KaniPS
> [📑 English Version | 英文文档](Command_EN.md)

---
### 📑 目录
- [👥 角色命令](#-角色命令)
- [💎 货币命令](#-货币命令)
- [🎲 抽卡命令](#-抽卡命令)
- [❓ 帮助命令](#-帮助命令)
- [📦 库存命令](#-库存命令)
- [💾 加载数据命令](#-加载数据命令)
- [🔧 设置账号命令](#-设置账号命令)
- [🎮 赛季命令](#-赛季命令)
- [🔓 解锁全部命令](#-解锁全部命令)

# 👥 角色命令
> 管理您的角色系统，打造完美的战斗团队

## ⌨️ 命令格式
```
/character [command] [characterID] [options]
```

## 🎯 功能说明
此命令用于管理玩家的角色系统，支持添加、移除和显示角色功能。
## 📋 可用子命令

### 📊 显示角色列表 (show)
```
/character show
```
- 💫 功能：显示当前所有角色的ID列表

### ✨ 添加角色 (add)

#### 1. 🌟 添加所有角色
```
/character add all [basic|ue30|ue50|max]    
```
- 💫 功能：添加所有可用角色，并设置培养状态
- ✨ 培养选项：
  - `basic`: 基础培养状态
  - `ue30`: UE30培养
  - `ue50`: UE50培养
  - `max`: 最强状态
- 📝 示例：`/character add all max`
- ℹ️ 说明：所有角色将以最强状态添加

#### 2. ➕ 添加指定角色
```
/character add <characterID> [basic|ue30|ue50|max]
```
- 💫 功能：添加指定ID的角色
- ✨ 培养选项同上
- 📝 示例：`/character add 10000 max`
- ℹ️ 说明：如果角色已存在会提示错误

### 🗑️ 移除角色 (remove)

#### 1. 🧹 移除所有角色
```
/character remove all
```
- 💫 功能：移除所有角色
- 📝 返回消息：`All Characters Removed!`

#### 2. ❌ 移除指定角色
```
/character remove <characterID>
```
- 💫 功能：移除指定ID的角色
- 📝 示例：`/character remove 10000`
- 📝 返回消息：`<characterID> removed!`

### ❓ 帮助信息 (help)
```
/character help
```
或直接使用 `/character` 显示帮助信息

## ⚡ 错误提示
1. 🚫 无效的培养选项：
   - `Unknown options!`
2. ❌ 无效的角色ID：
   - `Invalid Character ID!`
3. ⛔ 未知命令：
   - `Unknown command!`
4. 🔄 重复添加角色：
   - `<characterID> already exists!`

## ⚡ 注意事项
1. 🔄 所有操作都会自动保存
2. 📝 命令不区分大小写
3. ℹ️ 添加已存在的角色会收到错误提示
4. ⚠️ 移除操作不可撤销

---

# 💎 货币命令
> 自由调整各类货币数量，畅享游戏体验

## ⌨️ 命令格式
```
/currency <货币类型> <数量>
```

## 🎯 功能说明
此命令用于管理玩家的货币系统，支持查看和修改货币数量。

## 📋 可用子命令

### 📊 显示货币列表 (show)
```
/currency show
```
- 💫 功能：显示所有可用货币及其当前数量
- 📝 返回格式：`[货币ID] - [货币类型]: [当前数量]`

## 💰 可用货币类型

### 💫 基础货币
- `Gold` - 💰 金币
- `Gem` - 💎 青辉石（总数）
- `GemPaid` - 💳 付费青辉石
- `GemBonus` - 🎁 奖励青辉石

### 🎫 体力票券
- `ActionPoint` - ⚡ 体力值
- `AcademyTicket` - 📚 学院券
- `ArenaTicket` - ⚔️ 竞技场券
- `RaidTicket` - 🎯 总力战券

### 🗺️ 每周副本券
- `WeekDungeonChaserATicket` - 🏃‍♂️ 追击战A券
- `WeekDungeonChaserBTicket` - 🏃‍♀️ 追击战B券
- `WeekDungeonChaserCTicket` - 🏃 追击战C券
- `WeekDungeonFindGiftTicket` - 🎁 寻宝战券
- `WeekDungeonBloodTicket` - 🗡️ 血战券
- `ChaserTotalTicket` - 🎯 追击战总券

### 🏫 学院副本券
- `SchoolDungeonATicket` - 📘 学院副本A券
- `SchoolDungeonBTicket` - 📗 学院副本B券
- `SchoolDungeonCTicket` - 📙 学院副本C券
- `SchoolDungeonTotalTicket` - 📚 学院副本总券

### 🌟 特殊副本券
- `TimeAttackDungeonTicket` - ⏱️ 限时挑战券
- `WorldRaidTicketA` - 🌍 世界副本A券
- `WorldRaidTicketB` - 🌎 世界副本B券
- `WorldRaidTicketC` - 🌏 世界副本C券

### ⚔️ 清除战券
- `EliminateTicketA` - 🗡️ 清除战A券
- `EliminateTicketB` - ⚔️ 清除战B券
- `EliminateTicketC` - 🛡️ 清除战C券
- `EliminateTicketD` - 🔰 清除战D券

### 🏆 其它
- `MasterCoin` - 🎖️ 大师币

## 📝 使用示例
```
/currency Gem 99999          # 设置青辉石为99999
/currency ActionPoint 9999   # 设置体力值为9999
/currency Gold 99999999     # 设置金币为99999999
```

## ⚡ 注意事项
1. 📝 货币类型区分大小写
2. 🔢 数量必须为整数
3. 🔄 修改立即生效并保存
4. ⚠️ 无效输入将提示错误
5. 💡 请合理使用此功能

---
# 🎲 抽卡命令
> 自定义抽卡概率和保底设置

## ⌨️ 命令格式
```
/gacha [type] [value] [rate]
```

## 🎯 功能说明
此命令用于管理抽卡系统，包括设置抽卡概率、保底角色，以及查看相关信息。

## 📋 可用子命令

### 📊 查看角色列表 (show)
```
/gacha show
```
- 💫 功能：显示所有可抽取角色的列表
- 📝 返回格式：按稀有度分类显示角色ID和名称

### ⚙️ 设置抽卡概率 (rate)
```
/gacha rate <SSR|SR|R> <概率>
```
- 💫 功能：设置指定稀有度的抽取概率
- 📝 参数说明：
  - 稀有度：SSR、SR、R
  - 概率：0-100之间的数值
- 📝 示例：`/gacha rate SSR 3.5`

### 🎯 设置保底角色 (guarantee)
```
/gacha guarantee <角色ID>
```
- 💫 功能：设置抽卡保底角色
- ⚠️ 警告：请谨慎使用，错误的设置可能导致客户端异常

### 🔄 重置设置 (reset)
```
/gacha reset
```
- 💫 功能：重置所有抽卡设置为默认值
- 📝 影响范围：
  - 清除自定义概率
  - 移除保底角色设置

### 👀 查看当前设置 (settings)
```
/gacha settings
```
- 💫 功能：显示当前的抽卡设置
- 📝 显示内容：
  - 各稀有度的自定义概率
  - 当前的保底角色ID

## ⚡ 错误提示
1. 🚫 无效概率：
   - `Invalid rate! Please use a number between 0 and 100.`
2. ❌ 无效角色ID：
   - `Invalid character ID!`
   - `Character not found!`
3. ⚠️ 参数缺失：
   - `Please specify both rarity and rate!`
   - `Please specify character ID!`

## ⚡ 注意事项
1. 🔄 所有设置立即生效
2. ⚠️ 设置保底角色时需特别谨慎
3. 📝 概率设置范围为0-100
4. 💡 可随时通过reset命令恢复默认设置

---
# ❓ 帮助命令
> 获取详细的命令使用说明

## ⌨️ 命令格式
```
/help [command]
```

## 🎯 功能说明
此命令用于查看所有可用命令的帮助信息，或获取特定命令的详细说明。

## 📋 使用方法

### 1. 📑 查看所有命令
```
/help
```
- 💫 功能：显示所有可用命令的列表
- 📝 返回格式：
  - `命令名称 - 命令说明 (Usage: 使用方法)`
- 📌 结尾会显示提示：
  - `/{command} help - To get more information about that command`

### 2. 🔍 查看特定命令
```
/help <command>
```
- 💫 功能：显示指定命令的详细帮助信息
- 📝 返回内容：
  - 命令名称和说明
  - 具体使用方法
  - 所有参数的说明
- 📝 示例：`/help currency`

## ⚡ 错误提示
- ❌ 无效命令名称：
  - `Invalid Argument.`

## ⚡ 注意事项
1. 📝 命令名称必须是纯英文字母（a-zA-Z）
2. 🔤 命令名称不区分大小写
3. ❌ 指定不存在的命令会返回错误
4. 💡 不带参数时显示所有命令概览

---

# 📦 库存命令
> 一键管理所有游戏物品

## ⌨️ 命令格式
```
/inventory [command] [type] [options]
```

## 🎯 功能说明
此命令用于管理玩家的库存物品，包括角色、装备、道具等游戏内容。

## 📋 可用子命令

### 1. ✨ 添加物品 (add)
```
/inventory add <type> [options]
```

- 💫 可用类型 (type)：
  - 📦`all`: 所有物品
  - 👥`characters`: 角色
  - 🛡️`equipments`: 装备
  - 🎁`items`: 道具
  - 🔧`gears`: 装置
  - 🏰`lobbies`: 记忆大厅
  - 📚`scenarios`: 剧情
  - 🏠`furniture`: 家具

- ✨ 培养选项 (options)：
  - 💫`basic`: 基础状态
  - 🆙`ue30`: UE30培养
  - 📈`ue50`: UE50培养
  - 💪`max`: 最强状态

### 2. 🗑️ 移除物品 (remove)
```
/inventory remove <type>
```

- 💫 可用类型同上
- ⚠️ 移除操作会清空指定类型的所有物品

### 3. ❓ 帮助信息 (help)
```
/inventory help
```
或直接使用 `/inventory` 显示帮助信息

## ⚡ 错误提示
1. 🚫 无效的培养选项：
   - `Unknown options!`
2. ❌ 无效的类型：
   - `Unknown type!`
3. ⛔ 无效的操作：
   - `Unknown operation!`

## ⚡ 注意事项
1. 🔄 所有操作都会自动保存
2. 📝 命令参数不区分大小写
3. ⚠️ 移除操作不可撤销
4. 💡 培养选项仅适用于添加操作
5. ✨ 不指定培养选项时使用基础状态

---
# 💾 加载数据命令
> 从保存的文件中加载账号数据

## ⌨️ 命令格式
```
/loaddata <file_name|list>
```

## 🎯 功能说明
此命令用于从保存的JSON文件中加载账号数据，包括角色、装备、道具等全部游戏内容。

## 📋 可用子命令

### 1. 📂 查看可用数据文件
```
/loaddata list
```
- 💫 功能：显示 `Resources/AccountData/` 目录下所有可用的数据文件
- 📝 返回格式：显示所有可用的数据文件名称

### 2. 📥 加载数据文件
```
/loaddata <file_name>
```
- 💫 功能：加载指定的数据文件
- 📝 示例：`/loaddata save1.json`
- 📦 加载内容：
  - 👤 用户信息（昵称、等级、经验等）
  - 👥 角色数据
  - ⚔️ 武器数据
  - 🎁 道具数据
  - ⚙️ 装置数据
  - 🛡️ 装备数据
  - 🏰 记忆大厅数据
  - 🏠 咖啡厅数据
  - 🪑 家具数据
  - 👥 梯队数据

## ⚡ 错误提示
1. 🚫 文件未找到：
   - `File <file_name> was not found! Be sure to include ".json".`
2. ❌ 数据包缺失：
   - `Your data file does not contain the AccountAuthResponse - <packet_id> Packet.`
   - `Your data file does not contain the AccountLoginSyncResponse - <packet_id> Packet.`
3. ⚠️ 物品数据缺失：
   - `Could not find any packet associated with item data.`
4. 📁 目录不存在：
   - `That path does not exist!`

## ⚡ 注意事项
1. 🔄 加载操作会覆盖当前账号的所有数据
2. 📝 文件名需要包含 `.json` 后缀
3. 💾 数据文件必须位于 `Resources/AccountData/` 目录下
4. ✅ 加载成功会显示确认消息：`Successfully Loaded All Data from the save file.`

---
# 🔧 设置账号命令
> 自定义您的账号信息，打造个性化体验

## ⌨️ 命令格式
```
/setaccount [type] [value]
```

## 🎯 功能说明
此命令用于修改玩家账号的各项属性数据。

## 📋 可用子命令

### 1. 📊 查看可用属性 (show)
```
/setaccount show
```
- 💫 功能：显示所有可修改的账号属性
- 📝 返回格式：`属性名 - 数据类型`

### 2. ⚙️ 设置属性值
```
/setaccount <属性名> <值>
```
- 💫 功能：修改指定属性的值
- 📝 示例：`/setaccount Nickname Sensei`
- ✅ 成功提示：`Set Player with UID <id>'s <property> to <value>`
### 👤 基础信息
- `Nickname` - 📝 昵称
  - 类型：文本
  - 示例：`/setaccount Nickname Sensei`

- `Level` - 📊 等级
  - 类型：整数
  - 示例：`/setaccount Level 75`

- `Exp` - ✨ 经验值
  - 类型：整数
  - 示例：`/setaccount Exp 999999`

### 🎨 个人设置
- `CallName` - 📢 称呼名称
  - 类型：文本
  - 示例：`/setaccount CallName Teacher`

- `Comment` - 📝 个人简介
  - 类型：文本
  - 示例：`/setaccount Comment "Hello World"`

- `LobbyMode` - 🏰 大厅模式
  - 类型：整数
  - 示例：`/setaccount LobbyMode 1`

### 🎭 展示相关
- `RepresentCharacterServerId` - 👥 代表角色ID
  - 类型：整数
  - 示例：`/setaccount RepresentCharacterServerId 10000`

- `MemoryLobbyUniqueId` - 🏰 记忆大厅ID
  - 类型：整数
  - 示例：`/setaccount MemoryLobbyUniqueId 1`

### 📊 账号状态
- `State` - 🔰 账号状态
  - 类型：AccountState枚举
  - 示例：`/setaccount State Normal`

- `VIPLevel` - 👑 VIP等级
  - 类型：整数
  - 示例：`/setaccount VIPLevel 5`

### ⏰ 时间相关
- `BirthDay` - 🎂 生日
  - 类型：日期时间
  - 示例：`/setaccount BirthDay 2024-01-01`

- `LastConnectTime` - 🔄 最后连接时间
  - 类型：日期时间
  - 示例：`/setaccount LastConnectTime "2024-01-01 12:00:00"`
### 3. ❓ 帮助信息 (help)
```
/setaccount help
```
或直接使用 `/setaccount` 显示帮助信息

## ⚡ 错误提示
1. 🚫 无效的属性名：
   - `Invalid Account Property!`
2. ❌ 无效的属性值：
   - `Invalid Value`
## ⚡ 注意事项
1. 🔄 所有修改都会自动保存
2. 📝 属性名必须是纯英文字母
3. ⚠️ 属性值必须与数据类型匹配
4. 💡 使用 show 命令查看所有可用属性
5. ℹ️ 属性名不区分大小写

---

# 🎮 赛季命令
> 设置各类游戏内容的赛季

## ⌨️ 命令格式
```
/setseason [type] [seasonId]
```

## 🎯 功能说明
此命令用于设置不同游戏内容的赛季ID。

## 📋 可用子命令

### 1. 📊 查看可用赛季 (show)

```
/setseason show
```
- 💫 功能：显示所有可用的赛季信息
- 📝 显示内容：
  - 总力战赛季列表及对应Boss
  - 大型总力战赛季列表及对应Boss
  - 联合演习赛季列表及类型

### 2. ⚔️ 总力战赛季 (total)
```
/setseason total <seasonId>
```
- 💫 功能：设置总力战赛季
- 📝 返回信息：
  - 👾 Boss信息
  - 🔢 赛季ID
  - 📅 开始时间

### 3. 🌟 大型总力战赛季 (grand)
```
/setseason grand <seasonId>
```
- 💫 功能：设置大型总力战赛季
- 📝 返回信息：
  - 👾 Boss信息（三个Boss组）
  - 🔢 赛季ID
  - 📅 开始时间

### 4. 🎯 联合演习赛季 (drill)
```
/setseason drill <seasonId>
```
- 💫 功能：设置联合演习赛季
- 📝 返回信息：
  - 🎯 演习类型
  - 🔢 赛季ID
  - 📅 开始时间

### 5. ❓ 帮助信息 (help)
```
/setseason help
```
或直接使用 `/setseason` 显示帮助信息

## ⚡ 错误提示
1. 🚫 无效的赛季ID：
   - `Invalid Season ID!`
   - `Season ID does not exist`
2. ❌ 无效的类型：
   - `Invalid type!`

## ⚡ 注意事项
1. 🔄 设置后会自动保存
2. 📝 命令不区分大小写
3. 🔢 赛季ID必须为数字
4. 🔰 设置新赛季会重置相关数据：
   - ⏱️ 时间加成
   - 🏆 最佳排名分数
   - 📊 总排名分数

---
# 🔓 解锁全部命令
> 一键解锁游戏内容

## ⌨️ 命令格式
```
/unlockall [target content]
```

## 🎯 功能说明
此命令用于解锁指定类型的所有游戏关卡。

## 📋 可用子命令

### 1. 📚 主线剧情 (campaign)
```
/unlockall campaign
```
- 💫 功能：解锁所有主线关卡
- 📝 解锁效果：
  - 所有难度关卡全部解锁
  - 获得三星评价
  - 完成所有奖励领取
- ✅ 成功提示：`Unlocked all of stages of campaign!`

### 2. 🗺️ 每周副本 (weekdungeon)
```
/unlockall weekdungeon
```
- 💫 功能：解锁所有每周副本
- 📝 解锁效果：
  - 所有关卡可进入
  - 达成所有星级目标
- ✅ 成功提示：`Unlocked all of stages of week dungeon!`

### 3. 🏫 学院副本 (schooldungeon)
```
/unlockall schooldungeon
```
- 💫 功能：解锁所有学院副本
- 📝 解锁效果：
  - 所有关卡可进入
  - 达成所有星级目标
- ✅ 成功提示：`Unlocked all of stages of school dungeon!`

### 4. ❓ 帮助信息 (help)
```
/unlockall help
```
或直接使用 `/unlockall` 显示帮助信息

## ⚡ 错误提示
- ❌ 无效的内容类型：
  - `Invalid target!`

## ⚡ 注意事项
1. 🔄 解锁操作立即生效并保存
2. 📝 命令不区分大小写
3. ⚠️ 解锁后无法撤销
4. 💡 所有解锁内容均达到最高完成度

---
## 📝 文档更新记录

### v1.0.0 (2025-01-20)
- ✨ 首次发布完整命令文档
- 📚 添加所有基础命令说明
- 🎨 优化文档排版和样式
- 🔍 补充详细使用示例
- 🐛 修复文档格式问题
- ✨ 添加更多使用示例
- 📝 完善注意事项说明
### v1.01 (2025-01-23)
- ✅ 匹配新项目
- ⚡ 添加错误提示🔧
- 🌐 添加了英文版本翻译
### v1.02 (2025-01-27)
- ✅ 再次匹配新项目
- ✨ 优化命令格式和说明
- 📚 补充具体功能效果
- 🔧 修复链接跳转

---
*💡 如有任何问题或建议，欢迎随时反馈！*

## 📜 License

This project is licensed under [CC BY-NC 4.0](LICENSE) - see the [LICENSE](LICENSE) file for details.

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)