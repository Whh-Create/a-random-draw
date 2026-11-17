# 随机点名

一个不重复的随机点名 / 抽号小工具。输入总人数，点击「开始」，数字滚动 0.5 秒后定格，抽出的号码自动进入右侧存档，同一个号码不会被抽到第二次。全部抽完后显示「已完成抽签」。

## 使用

直接用浏览器打开 `index.html` 即可，无需安装任何依赖，也无需联网。

1. 在「总人数」里填一个数字（例如班级 42 人就填 42）
2. 点击「开始」，数字滚动 0.5 秒后停下
3. 结果自动记入右侧存档，已抽过的号码不会再出现
4. 抽完所有人后按钮变为「已完成」，点击「重置」可以重新开一轮

小技巧：在人数输入框里按回车也能直接开始。

## 说明

- 存档会保存在浏览器本地（localStorage），刷新页面不会丢失；点「重置」才会清空
- 一旦开始抽签，人数输入框会锁定，避免中途改人数导致号码错乱
- 纯前端实现，所有数据只存在本机浏览器里

## 部署到 GitHub Pages

```bash
git init
git add index.html README.md
git commit -m "init: 随机点名"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

推送完成后，进入仓库的 **Settings → Pages**，把 Source 设为 `Deploy from a branch`，分支选择 `main`、目录选择 `/ (root)`，保存后等一两分钟，即可通过
`https://<你的用户名>.github.io/<仓库名>/` 访问。

## 文件结构

```
.
├── index.html   # 全部页面、样式与逻辑
└── README.md
```
