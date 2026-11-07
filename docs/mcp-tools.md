# MCP 工具清单（规划）

工具名遵循 `域.动作` 的小写风格；同一动作的读写语义必须在工具描述里写明。
所有工具默认只读，写操作需要 `dryRun` 与确认令牌。

| 工具 | 作用 | 读写 | 状态 |
| --- | --- | --- | --- |
| `project.list` | 列出本地工程 | 只读 | 规划中 |
| `project.current` | 当前打开的工程与页面 | 只读 | 规划中 |
| `schematic.pages` | 原理图页面列表 | 只读 | 规划中 |
| `schematic.components` | 页面上的元件（位号、型号、封装） | 只读 | 规划中 |
| `schematic.nets` | 网络与连接关系 | 只读 | 规划中 |
| `schematic.netlist` | 导出权威网表 | 只读 | 规划中 |
| `pcb.outline` | 板框与尺寸 | 只读 | 规划中 |
| `pcb.stackup` | 叠层与板厚 | 只读 | 规划中 |
| `pcb.components` | 已布局器件与坐标 | 只读 | 规划中 |
| `pcb.nets` | PCB 网络与走线统计 | 只读 | 规划中 |
| `pcb.drc` | 运行并返回 DRC 报告 | 只读（会触发检查） | 规划中 |
| `bom.export` | 导出 BOM | 只读 | 规划中 |
| `gerber.export` | 导出 Gerber | 写文件 | 规划中 |
| `cpl.export` | 导出贴片坐标文件 | 写文件 | 规划中 |

## 待定问题

- 工程文件直接解析，还是必须经由运行中的 EasyEDA Pro 客户端？
- 写操作确认令牌的有效期与作用域。
- 导出文件的默认目录与命名规则。
