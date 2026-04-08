
音乐 Tab 触发规则
📍 显示条件
音乐 Tab 不是固定显示，满足以下任一条件时才会出现：

站源名称包含 [听]
站源分类字段为"音乐"或 music
同时音乐入口开关已开启
📝 配置示例
音乐源满足以上任一条件即可被识别为音乐源。具体配置示例：

方式一：使用 [听] 标识

{
  "key": "资源管理.py",
  "name": "资源管理.py[听]",
  "type": 3,
  "api": "./py/资源管理.py",
  "searchable": 1,
  "changeable": 1,
  "quickSearch": 1,
  "filterable": 1
}
方式二：使用分类字段

{
  "key": "music_source",
  "name": "音乐站",
  "type": 3,
  "api": "./js/music.js",
  "searchable": 1,
  "changeable": 1,
  "quickSearch": 1,
  "filterable": 1,
  "类型": "音乐"
}
或使用英文分类：

{
  "key": "music_source",
  "name": "音乐站",
  "type": 3,
  "api": "./js/music.js",
  "searchable": 1,
  "changeable": 1,
  "quickSearch": 1,
  "filterable": 1,
  "genre": "music"
}
关键配置说明：

方式一：在 name 字段中包含 [听] 标识即可
方式二：添加 类型 字段，值为 ["音乐"] 或 ["music"]
两种方式任选其一，也可以同时使用
确保应用中的音乐入口开关已开启

支持使用英文字段 genre 标识源类型，优先读取 genre，不存在时读取 类型。

配置示例
{
  "sites": [
    {"name": "小说源", "genre": "novel"},
    {"name": "短剧源", "genre": "shortdrama"},
    {"name": "漫画源", "genre": "comic"}
  ]
}
支持的值
类型	中文	英文
小说	"小说"	"novel" / "book"
短剧	"短剧"	"shortdrama" / "short_drama"
漫画	"漫画"	"comic" / "manga"

js 收集，网盘类是jar，py，php
PeekPili羊壳配置大杂烩解压码6666直接解压到根目录（不要套壳\bdb
