# 机械蜻蜓 · 三维立体展示

可自由旋转、缩放的三维机械蜻蜓展示页。双击任意零部件即可镜头聚焦并查看名称与说明。共 **24** 个独立可选中零件（P01–P24），视觉兼顾科技感与仿生仿真度。

## 环境要求

- Node.js 18+（推荐 20+）
- 现代桌面浏览器（Chrome / Edge / Firefox / Safari）

## 安装

```bash
npm install
```

## 开发预览

```bash
npm run dev
```

终端会给出本地地址（默认 `http://localhost:5173`），用浏览器打开即可。

## 构建

```bash
npm run build
```

产物输出到 `dist/`。可用 `npm run preview` 本地预览构建结果。

## 操作说明

| 操作 | 效果 |
| --- | --- |
| 左键拖拽 | 轨道旋转（俯仰约 ±80° 限位） |
| 滚轮 / 双指捏合 | 缩放（不会穿入模型内部） |
| 悬停零件 | 高亮提示 |
| 单击零件 | 选中高亮，不改变镜头、不打开面板 |
| **双击零件** | 镜头平滑飞入（0.6–1.0s），打开说明面板 |
| 「扑翼演示」按钮 | 播放 1～2 次完整扑翼后回到怠速 |
| 单击空白 / 面板关闭 | 退出细节态，镜头回到进入前视角 |

界面弱提示：「拖拽旋转 · 滚轮缩放 · 双击零件查看详情」

## 技术栈

- Vite + TypeScript
- Three.js（程序化组装模型，无外部商业模型资源）

## 零件一览（P01–P24）

与产品说明一致：`part_head_armor`、`part_eye_left` / `part_eye_right`、`part_antennae`、`part_mouthparts`、`part_thorax`、`part_power_core`、四翅、左右扑翼关节、六足、`part_abdomen`、`part_tail`、`part_gear_train`、`part_cooling`、`part_drive_shafts`。

默认怠速：齿轮啮合转动、传动轴随动；翅膀仅低幅微动。

## 说明

本项目为纯前端单页，无后端。模型由 Three.js 几何体组合生成，非授权商业模型。
