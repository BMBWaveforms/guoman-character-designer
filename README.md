# guoman-character-designer

3D 半写实国漫人物四视图中文提示词生成 Skill。

## 功能

根据**文字描述**创作一名角色的一段完整中文生图提示词。固定精致BJD人偶风/CG建模质感、纯白影棚设定板、左侧大幅面部特写与右侧正面/侧面/背面全身三视图。年龄、性别、世界观、身份、体型、服装均可变化。模仿六组样本的详细自然语言写法，不复刻样本中的人物。

不支持参考图反推、角色变体/换装、直接生图。

## 安装

将整个 `guoman-character-designer` 文件夹复制到支持 Agent Skills（`SKILL.md` 格式）的工具的 Skills 目录，重新加载 Skills。常见安装方式示例：

- Codex 本地个人 Skills：`~/.codex/skills/guoman-character-designer/`（安装到当前环境识别的 Skills 目录）。
- Claude Code：`~/.claude/skills/guoman-character-designer/`（具体路径以当前版本为准）。

也可以直接在聊天中附上 `SKILL.md` 作为规则使用，但这不等同于系统自动加载的 Skill。

## 使用

直接输入：“使用 guoman-character-designer：一位45岁的古代男性御医，头发微白，深青色长袍，温和克制。”

默认返回：**仅一段可复制的中文生图提示词**，无分析、无标题、无图片。

## 内容

- `SKILL.md`：Skill 的入口与执行规则。
- `references/six-case-patterns.md`：六张用户样本的提示词写作规律拆解。
- `references/character-adaptation.md`：年龄、性别和世界观适配。
- `references/full-example.md`：跨年龄完整输出示例。
- `tests/smoke-tests.md`：手动验收用例。

## 批量角色创作

可同时提供多个人物概念，并明确主角/配角数量、年龄分布、面孔设定及时代。批量数量与风格偏好由当前请求决定；每个人物分别生成完整提示词，不把某次任务的“20位、全东亚面孔”等要求固定到 Skill。

例如：

> 请为现代与古代恋爱漫剧写20位人物提示词，14位主角、6位配角，全部东亚面孔。青年主角强调俊男靓女，成熟与年长配角保留年龄和身份特征。

图片生成、Arena操作、下载和飞书评分属于外部工作流，需要另行明确要求。仓库不包含私人评测文档、浏览器会话或生成图片。

## 许可证

采用 [MIT License](LICENSE)，可使用、修改与分发。
