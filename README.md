# KiCad 交互式 HTML BOM 插件
## 支持 EasyEDA、Eagle、Fusion360 和 Allegro PCB 设计软件

![icon](https://i.imgur.com/js4kDOn.png)

本插件可生成一份便捷的物料清单（BOM），支持可视化关联并轻松搜索元件及其在 PCB 上的位置。在手工焊接原型板时特别实用——用户可以快速定位 PCB 上各元件组的位置。同时支持通过点击板图上的封装来反向查找对应的元件组。

插件利用 Pcbnew 的 Python API 读取 PCB 数据，并渲染丝印层、制造层、封装焊盘、文字及图形。BOM 表格字段和分组方式均可完全自定义，制造商料号等附加列可在原理图编辑器中添加，并通过网络表文件、Eeschema 内置 BOM 工具生成的 XML 文件或直接从板文件中导入。

插件还支持包含走线/覆铜数据以及网络表信息，可实现板图上网络的动态高亮显示。

完整功能说明请参阅 [Wiki 文档](https://github.com/openscopeproject/InteractiveHtmlBom/wiki)。

生成的 HTML 页面完全自包含，无需网络连接即可使用，可随项目文档一同打包发布，也可托管于任何 Web 服务器上。

[百闻不如一见，点击查看演示。](https://openscopeproject.org/InteractiveHtmlBomDemo/)

## 安装与使用

安装说明请参阅 [项目 Wiki](https://github.com/openscopeproject/InteractiveHtmlBom/wiki/Installation)。

### 通过 KiCad PCM 安装（推荐）
在 KiCad 插件管理器 → 管理库链接 中添加：
```
https://raw.githubusercontent.com/harry10086/InteractiveHtmlBom/gh-pages/repository.json
```

### 手动安装
下载附件 `InteractiveHtmlBom_v2.11.2_pcm.zip`，
在 KiCad 插件管理器中选择"从文件安装"。

## 许可证与致谢

插件代码以 MIT 许可证授权，详细信息请参阅 `LICENSE` 文件。

HTML 页面使用了以下开源库，均已内嵌至生成的 BOM 页面中：
[Split.js](https://github.com/nathancahill/Split.js)、
[PEP.js](https://github.com/jquery/PEP) 和（精简版）[lz-string.js](https://github.com/pieroxy/lz-string)。

`units.py` 来自 [KiBom](https://github.com/SchrodingersGat/KiBoM) 插件（MIT 许可证）。

`svgpath.py` 主要基于 [svgpathtools](https://github.com/mathandy/svgpathtools) 模块（MIT 许可证）。
