# alias-skip

> test
> 别名路径跳转插件，支持任何项目，可以自由配置映射规则，自由配置可缺省后缀名列表
> TODO: 拓展自从vueconfig 读取
> TODO: 拓展自动从webpack 等构建工具中自动读取alias
> TODO: map 提供函数入参 支持用户自定义mapping 规则

## 使用方法

鼠标移动到路径上，按住`ctrl`并单击就会跳转

## 配置项

> 配置项可以写入`settings.json`中，来扩展插件的能力

如果写入配置后不生效，试试重启vscode

- 路径映射，`/`表示项目根目录，示例

```json
    "alias-skip.mappings": {
        "@":"/src"  // 默认只有`@`映射，映射到`/src`，你可以添加更多映射，映射路径必须以`/`开头
        // ...更多映射关系
    }
```

- 可缺省后缀名的文件列表，以下文件不需要写后缀名

```json
    "alias-skip.allowedsuffix": ["js","vue","jsx","ts"]  // 默认有这四项
```

- 判断项目根目录的依据，默认为package.json，即存在该文件的目录为项目根目录，例如小程序项目可以改成app.json

```json
    "alias-skip.rootpath": "package.json"
```

## 效果图

![效果图](https://vscode.lihuiwang.net/%E6%95%88%E6%9E%9C%E5%9B%BE.gif)
