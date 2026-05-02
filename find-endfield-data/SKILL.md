---
name: find-endfield-data
description: "The structures and the data from game 'Arknights Endfields'. USE FOR: Research endfield data structures. get  game data. Search game texture/image"
---

# Find Endfield Data

## Tables
终末地的`Table`中数据结构为一个 `{ [key: string]: any }` 的字典。

### 获得所有Tables

- 接口: https://endfield-assets.fffdan.com/vfs/Table/
- 返回值：`string[]`

注意，这里返回的是`Data/TableCfg/{FileName}.bytes`的数组，其中的`{FileName}`就是Table的名字

### 获取Table的Keys
- 接口：https://endfield-assets.fffdan.com/table/{TableName}
- 返回值：`string[]`


### 获取Table的Value

- 接口：https://endfield-assets.fffdan.com/table/{TableName}/{Key}
- 返回值：`any`

### 获取所有Table的值

注意：这个接口返回数据量会非常大，有可能会撑爆你的上下文，谨慎使用。

- 接口：https://endfield-assets.fffdan.com/table/{TableName}/all
- 返回值: `{ [key: string]: any }`

## 游戏资源

资源的搜索接口为：
- 接口：https://endfield-assets.fffdan.com/vfs/Bundle/search/{*query}
- 可选query: `suffix={suffix}`，用于筛选后缀名
- 返回值: `string[]`

### 可下载资源

在搜索后拿到地址，如：`assets/beyond/initialassets/ui/sprites/login/login_test_deco.png`

可以和该域名拼接：`https://endfield-assets.fffdan.com/vfs/Bundle/file/`

真实下载地址为：`https://endfield-assets.fffdan.com/vfs/Bundle/file/assets/beyond/initialassets/ui/sprites/login/login_test_deco.png`，

目前可下载的资源后缀为：`.png`, `.tga`，其余资源下载会返回`404`。

