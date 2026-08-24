当前 `军训文字模拟器` 项目里的文件分工如下：

- `pages/index.html`：游戏主页面。包含完整的 HTML 结构、开局问答/序章/六时段事件/固定事件/随机事件/隐藏事件/结局判定的全部 JS 逻辑，以及成长报告、雷达图等 UI。
- `colors_and_type.css`：定义主题色（迷彩绿、沙色、红旗红等）、字体、间距、圆角、阴影等变量，并作为 `.preflight` 的样式来源。
- `.design`：画布元数据文件。记录页面节点、交互注册、资源引用等信息，让前端能把项目渲染成可继续编辑的设计稿。
- `.preflight/preflight.html`：CSS 预检证据页。用于验证 `colors_and_type.css` 的主题变量、语义化 token 回退等是否满足设计规范。
- `runtime-dispatch-manifest.json`：运行时分发清单。记录本次任务使用的 lane、页面、校验脚本等，供设计工作流回溯。
- `runtime-orchestration-summary.json`：编排摘要。记录技能版本、意图识别结果、已加载的规范文件、校验纪律等执行上下文。
- `validation-report.json`：校验报告。汇总设计工作区各检查项的结果（结构、HTML 质量、资源覆盖等）。

其中真正面向玩家运行的是 `pages/index.html`，其余文件多为设计系统/工作流留痕与校验产物。