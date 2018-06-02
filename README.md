## 注意
不要有一级标题哈，一级标题就是文件名

## 图片资源
放在 `./blog/doc/assets/` 目录下。资源只能有一级目录，不能有二级目录。比如：

- `./blog/doc/assets/image.png` 可以
- `./blog/doc/assets/test/image.png` 可以
- `./blog/doc/assets/test/test/image.png` 不可以，不能有二级目录

![](/blog/doc/assets/image.png)

## 编写文档

　　目录/文构的结构进行编写：

```
# 由于需要兼顾美观性，文档的目录不要超过2层

├── 总体说明.md
├── 一级目录
│   ├── 测试文档1.md
│   ├── 测试文档2.md
│   └── 二级目录
│       ├── 测试文档3.md
│       └── 测试文档4.md
└── 其它说明.md
```

　　`mapping.json`用于描述文档的目录结构、顺序、每个文档的`URL简称`。

> `URL简称`是文档唯一性标识，每个文档的`URL简称`应该都不一样。
> 
> `URL简称`的命名规则应遵循`word-to-word`规则，建议采用文档的英文翻译。

```json
{
    "总体说明": "about",
    "一级目录": {
        "测试文档1": "test1",
        "测试文档2": "test2",
        "二级目录": {
            "测试文档3": "test3",
            "测试文档4": "test4"
        }
    },
    "其它说明": "other"
}
```