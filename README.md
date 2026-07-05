# 精灵方舟 · 游戏大厅

网页游戏合集，通过 GitHub Pages 永久免费托管。

## 在线访问

https://1847531284.github.io/game2048/

## 游戏列表

| 游戏 | 文件 | 说明 |
|------|------|------|
| 精灵方舟：变异 | `spirit_mut.html` | 紫色变异主题，双属性方块+配对合并+病毒系统 |
| 精灵方舟：进化 | `spirit_evo.html` | 绿色生态主题，腐化净化+生物进化链 |
| 经典 2048 | `classic2048.html` | 原版 2048 |

## 如何添加新游戏

1. 把新游戏的 HTML 文件放进仓库根目录（如 `my_game.html`）
2. 编辑 `index.html`，在 `GAMES` 数组里加一项：

```js
{
  title: '我的新游戏',
  subtitle: 'MY NEW GAME',
  icon: '🎮',
  desc: '一句话描述玩法。',
  url: 'my_game.html',
  color: '#ff6b6b',   // 主题色
  tags: ['标签1', '标签2'],
  isNew: true
}
```

3. 提交并推送到 `gh-pages` 分支：

```bash
git add my_game.html index.html
git commit -m "feat: 新增我的新游戏"
git push origin gh-pages
```

4. 等 1-2 分钟，刷新页面即可看到新游戏卡片。

## 技术说明

- 所有游戏均为**单文件 HTML**（CSS/JS 全内联），无外部依赖
- 进度通过 `localStorage` 自动保存到浏览器本地
- GitHub Pages 提供 HTTPS + 免费托管，每月 100GB 流量
- 推送后 1-2 分钟生效，强制刷新可加 `?v=2` 参数

## 目录结构

```
game2048/
├── index.html          # 游戏大厅入口页
├── spirit_mut.html     # 精灵方舟：变异
├── spirit_evo.html     # 精灵方舟：进化
├── classic2048.html    # 经典 2048
└── README.md           # 本说明文件
```
