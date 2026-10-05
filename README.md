# Memory Keeper 📚

文档驱动的记忆管理系统，让AI agent拥有"工作记忆"，构建知识图谱，实现外部记忆闭环。

## 🎯 核心价值

- **✨ 自动工作记录** - 生成标准6段式记录文档
- **🧠 知识图谱构建** - 记录涌现连接，自动构建概念网络
- **🌍 跨Agent协作** - 通过clawmem广场共享记忆
- **🔧 VS Code集成** - 图形界面，可视化工作记录

## 📦 安装方式

### 方式A：DSH Skill（推荐小白使用）
```bash
# 在DSH中安装
skill memory-keeper

# 然后直接在对话中使用：
"帮我写个工作记录：今天完成了skill开发"
"记录涌现连接：[[A]] × [[B]] → 新连接"
"打开最新的工作记录"
```

### 方式B：命令行（适合技术用户）
```bash
# 克隆仓库
git clone https://github.com/ri0977-code/memory-keeper
cd memory-keeper

# 初始化
python main.py init

# 写记录
python main.py write "今天完成了memory-keeper" --agent dsh

# 查看记录
python main.py read dsh
python main.py agent-list
```

### 方式C：VS Code插件（适合视觉党）
```bash
# 下载vsix文件
# 访问：https://github.com/ri0977-code/memory-keeper/releases

# 安装到VS Code
code --install-extension memory-keeper-1.0.2.vsix

# 在VS Code中使用：
# 右键 → Memory Keeper → Write/Read/Emerge
```

## 🚀 使用示例

### DSH Skill方式
```
用户: "帮我记录今天的工作：memory-keeper skill开发完成"
-> 自动创建工作记录，上传clawmem广场，更新知识图谱

用户: "记录一个连接：[[memory-keeper]] × [[clawmem]] → 文档驱动记忆闭环"
-> 自动追加到涌现连接.md，更新概念网络

用户: "看看我最近做了什么"
-> 自动打开最新的工作记录
```

### 命令行方式
```bash
# 写记录
python main.py write "工作内容" --agent dsh --summary "进展"

# 查看所有记录
python main.py list

# 同步clawmem广场
python main.py sync
```

### VS Code方式
- 右键菜单：Write/Read/Emerge
- 状态栏：显示agent计数
- 命令面板：快捷键 Ctrl+Shift+M

## 🔧 技术特性

- **完整结构化** - 6个section自动生成
- **跨Agent协作** - 通过clawmem共享记忆
- **知识图谱** - 涌现连接自动构建概念网络
- **双写闭环** - 本地记录+clawmem广场同步
- **无需依赖** - 纯Python实现，零依赖

## 📁 项目结构
```
memory-keeper/
├── main.py              # CLI核心
├── skills/              # Skill定义
│   └── memory-keeper/   # DSH skill
├── memory-vscode/       # VS Code插件
│   └── memory-keeper-1.0.2.vsix
├── .gitignore          # Git忽略规则
├── README.md            # 使用说明
└── LICENSE              # MIT协议
```

## 🌟 适用场景

- **个人记忆管理** - 替代传统笔记
- **AI Agent协作** - 跨agent知识共享
- **开发记录** - 代码迭代追踪
- **知识构建** - 自动构建知识图谱

## 📞 支持

- GitHub: https://github.com/ri0977-code/memory-keeper
- 状态: 已完成 ✅
- License: MIT