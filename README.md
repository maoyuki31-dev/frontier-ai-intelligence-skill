[README.md](https://github.com/user-attachments/files/33087124/README.md)
# frontier-ai-intelligence-skill
An Agent Skill for monitoring, validating, and analyzing frontier AI developments, turning high-signal updates into decision-ready intelligence reports.
# 海外 AI 前沿情报 Skill

一个用于发现、验证和分析全球 AI 前沿动态的可复用 Skill。它把零散新闻筛选成有来源、有评分、有验证状态、能支持产品和业务决策的行业情报。

## 文件

- `SKILL.md`：Skill 定义、监测范围、信息源分级、评分标准、分析流程和质量原则。
- `templates/daily-report-template.md`：每日情报报告模板。

## 安装

将本仓库克隆到你使用的 AI 助手的 skills 目录，或将 `SKILL.md` 与 `templates/` 一起复制到项目 Skill 目录。确保相对路径 `templates/daily-report-template.md` 可访问。

```bash
git clone https://github.com/maoyuki31-dev/frontier-ai-intelligence-skill.git
```

安装位置因 AI 助手而异。支持 Agent Skills 的工具通常要求 Skill 目录内包含带 `name` 和 `description` 的 `SKILL.md`。

## 使用

要求助手按 Skill 监测指定时间窗口内的 AI 动态，生成日报或趋势分析。默认以过去 24 小时为主窗口，结合近 7 天和 30 天事件；按总分 100 分评分，重点输出 S/A 级 Top 3，并把 B 级条目放入追踪表。

日报默认使用飞书云文档工作流（`feishu_create_doc`）。若运行环境没有相应工具，Skill 要求输出 Markdown，不声称已创建云文档。

## 质量约束

- 事实与分析分开，重要信息附来源链接和验证状态。
- 重要事件尽量包含官方来源和独立来源。
- 社区来源只作为线索，不单独支撑重大事实结论。
- 不为凑数收录低价值信息；不把融资和宣传直接当作技术突破。

## 来源

根据用户提供的《海外AI前沿情报 Skill（完整版）》PDF 整理为标准 Skill 文件。公开仓库未收录 PDF 中的私人文档参考链接。

## License

MIT，详见 [`LICENSE`](LICENSE)。
