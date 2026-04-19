# 🎨 App Gallery Studio

> **From Working Code to Winning Conversion.**
>
> 使用 AI 驱动的自动化工作流，为独立开发者提供一键式 App Store 营销素材解决方案。

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-15+-black?logo=next.js" alt="Next.js"/>
  <img src="https://img.shields.io/badge/Supabase-3ECF8E?logo=supabase&logoColor=white" alt="Supabase"/>
  <img src="https://img.shields.io/badge/TailwindCSS-06B6D4?logo=tailwindcss&logoColor=white" alt="TailwindCSS"/>
  <img src="https://img.shields.io/badge/Gemini-AI-4285F4?logo=google&logoColor=white" alt="Gemini"/>
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License"/>
</p>

---

## 🚀 项目愿景

大多数开发者能写出优秀的代码，但在 **ASO (应用商店优化)** 的最后一步往往卡在视觉设计上。

**App Gallery Studio** 旨在通过 **"Vibe Coding"** 的理念，让用户只需上传一张截图，即可通过 AI 自动生成具有 **Telegram 风格**、**高质感渐变** 和 **营销文案** 的专业展示图。

> 💡 让开发者专注于代码，让 AI 处理营销视觉。

---

## ✨ 核心特性

| 特性 | 描述 |
| :--- | :--- |
| 🤖 **AI 营销副驾驶 (Copilot)** | 自动分析截图界面，提取核心卖点（如 "Fast"、"Secure"），并生成多语言描述。 |
| 📱 **智能样机渲染** | 自动适配最新的 iPhone / iPad 设备框架，支持 3D 悬浮与阴影效果。 |
| 🖼 **画卷模式 (Panoramic)** | 支持多张截图背景连贯显示，打造沉浸式浏览体验。 |
| 📐 **ASO 规格对齐** | 严格遵守 Apple 官方尺寸规范（6.7"、6.5" 等），一键导出全套素材。 |

---

## 🛠 技术架构 (Stack)

### Frontend
- **框架**：Next.js 15+ (App Router)
- **样式**：Tailwind CSS
- **UI 组件**：Shadcn UI + Lucide React

### Backend & Infrastructure
- **Supabase Auth** — 用户鉴权与个人库管理
- **Supabase DB (PostgreSQL)** — 存储模板配置、文案记录与项目元数据
- **Supabase Storage** — 存储用户上传的原始截图 (Raw) 及生成的最终作品 (Export)

### Image Processing & AI
- **Canvas API + Fabric.js** — 客户端实时渲染
- **Gemini 1.5 Flash / Pro** — 视觉理解与文案本地化

---

## 🤖 Claude Code 开发协议 (Prompt Context)

> [!IMPORTANT]
> 当使用 Claude Code 辅助开发时，请严格遵守以下开发规范。

### 1. 状态管理与数据持久化

- **原则**：所有的样式配置（背景色、字体大小、样机型号）必须持久化在 Supabase 中，确保用户刷新页面后能继续编辑。
- **存储路径**：用户上传的图片统一存储在 `storage/screenshots` 路径下，采用 `UUID/filename` 命名。

### 2. UI / UX 准则

- **极简主义**：UI 应参考 Apple 设计指南 (HIG)。避免过度拥挤，确保实时预览窗口（Live Preview）占据屏幕中心。
- **响应式**：预览组件必须支持缩放（Scale to Fit），确保在不同分辨率的屏幕下都能完整显示生成效果。

### 3. 性能优化

- **客户端处理**：复杂的 Canvas 绘图应在 **Web Worker** 中进行，避免阻塞主线程。
- **图片压缩**：在上传至 Supabase 之前，必须在客户端进行图片质量优化，减少带宽成本。

---

## 📅 路线图 (Roadmap)

- [x] **Milestone 1 — MVP 框架**
  完成 Next.js + Supabase 基础环境搭建与图片上传功能。
- [ ] **Milestone 2 — 模板引擎**
  实现 Telegram 风格渐变背景与 iPhone 15 Pro 样机嵌套。
- [ ] **Milestone 3 — AI 文案介入**
  集成 Gemini API，实现根据截图自动填充 Header 文案。
- [ ] **Milestone 4 — 导出系统**
  实现 Serverless Function 驱动的高清多尺寸打包下载。

---

## 🏁 快速开始指南

### 1. 克隆仓库

```bash
git clone https://github.com/your-username/app-gallery-studio.git
cd app-gallery-studio
```

### 2. 环境配置

```bash
cp .env.example .env.local
```

在 `.env.local` 中填入以下环境变量：

```bash
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
GEMINI_API_KEY=your_gemini_api_key
```

### 3. 安装依赖

```bash
npm install
```

### 4. 运行开发环境

```bash
npm run dev
```

打开浏览器访问 [http://localhost:3000](http://localhost:3000) 即可开始使用。

---

## 🎨 关于 Vibe 风格

本项目深度致敬 **Telegram** 的视觉语言：

- 🎯 强调 **对比色**
- 🔠 **大字体标题**
- 🔲 极其 **平滑的边框圆角**

每一处细节都旨在传递"精致而不浮夸"的产品气质。

---

## 🤝 贡献指南

欢迎任何形式的贡献！如果你有好的想法或发现了 Bug，请：

1. Fork 本项目
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的修改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

---

## 📄 License

本项目基于 **MIT License** 开源 — 详见 [LICENSE](LICENSE) 文件。

---

<p align="center">
  Made with ❤️ for indie developers
</p>
