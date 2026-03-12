# my-p1

A new project

## 项目说明

这是一个新建的项目。

## Claude 配置说明

项目使用 `.claude/settings.local.json` 配置 AI 助手的权限：

### 允许的操作 (allow)
- **文件操作**: 读取、写入、编辑、搜索文件
- **命令执行**: Bash 命令、npm/pnpm 包管理
- **Git 操作**: 允许 git push 推送代码
- **网络访问**: WebFetch 和 WebSearch
- **浏览器自动化**: agent-browser 技能

### 禁止的操作 (deny)
- **敏感文件**: 禁止读取 .env 环境变量文件
- **SSH 密钥**: 禁止访问 ~/.ssh/ 目录
- **危险命令**: 禁止 rm/del/rmdir 删除操作

### 配置文件内容

```json
{
  "permissions": {
    "allow": [
      "Bash(*)",
      "Read(*)",
      "Write(*)",
      "Edit(*)",
      "Glob(*)",
      "Grep(*)",
      "WebFetch",
      "WebSearch",
      "Bash(git push *)",
      "Bash(git push)",
      "Bash(npm *)",
      "Bash(pnpm *)",
      "Skill(agent-browser)"
    ],
    "deny": [
      "Read(.env*)",
      "Read(**/.env*)",
      "Read(~/.ssh/**)",
      "Bash(rm *)",
      "Bash(del *)",
      "Bash(rmdir *)"
    ]
  }
}
```

## 开始使用

待补充...
