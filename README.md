# 🕹️ INDIE WEB ARCADE // 个人创意小游戏合集

这是一个基于 **GitHub + Netlify** 构建的零依赖、单文件 HTML5 创意小游戏合集仓库。

## 📁 目录结构

```text
my-arcade/
├── index.html                   # 复古街机厅合集大厅（带卡带切换、分类筛选、内嵌街机框体与配置生成器）
├── netlify.toml                 # Netlify 零构建静态部署配置
├── README.md                    # 项目说明与新游戏导入指南
└── games/
    └── one_bit_flashlight.html  # 01号卡带：《1-Bit Flashlight 手电筒怪谈》
```

## 🚀 如何部署到 GitHub + Netlify

1. 解压本压缩包后，在文件夹根目录打开终端：
   ```bash
   git init
   git add .
   git commit -m "feat: 初始化复古街机厅小游戏合集与手电筒怪谈"
   git branch -M main
   git remote add origin https://github.com/<你的GitHub用户名>/<你的仓库名>.git
   git push -u origin main
   ```
2. 登录 [Netlify](https://app.netlify.com/)，点击 **Add new site -> Import an existing project**，连接你的 GitHub 仓库。
3. Netlify 会自动识别根目录下的 `netlify.toml`（无需构建命令，发布目录为 `.`），点击 **Deploy** 即可上线！

## ➕ 以后如何添加新的小游戏？

1. 将新的单文件 HTML 小游戏（例如 `uvsu_loop.html`）放入 `games/` 文件夹。
2. 打开 `index.html`，可以在网页右上角点击 **「➕ 新增卡带配置」** 自动生成配置代码，或者直接在 `index.html` 的 `GAMES` 数组中新增一项：
   ```javascript
   {
     id: 'uvsu-loop',
     code: 'CART-02',
     title: 'UVSU 因果回环',
     subtitle: '自己追杀自己、再躲开自己的回合博弈',
     category: '时间循环',
     tags: ['时间循环', '回合弹幕', '解谜'],
     status: 'playable',
     file: 'uvsu_loop.html',
     controls: 'WASD 移动 / 鼠标瞄准射击',
     desc: '第一回合跑向终点，第二回合扮演恶魔狙击上一轮的自己，第三回合在自己的枪林弹雨中逃生。'
   }
   ```
3. 执行 `git add . && git commit -m "feat: 新增小游戏" && git push`，Netlify 会自动完成热更新。
