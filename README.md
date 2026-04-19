🎨 App Gallery Studio
From Working Code to Winning Conversion. 使用 AI 驱动的自动化工作流，为独立开发者提供一键式 App Store 营销素材解决方案。

🚀 项目愿景
大多数开发者能写出优秀的代码，但在 ASO (应用商店优化) 的最后一步往往卡在视觉设计上。App Gallery Studio 旨在通过“Vibe Coding”的理念，让用户上传一张截图，即可通过 AI 自动生成具有 Telegram 风格、高质感渐变 和 营销文案 的专业展示图。

✨ 核心特性
AI 营销副驾驶 (Copilot): 自动分析截图界面，提取核心卖点（如 "Fast", "Secure"），并生成多语言描述。

智能样机渲染: 自动适配最新的 iPhone/iPad 设备框架，支持 3D 悬浮与阴影效果。

画卷模式 (Panoramic): 支持多张截图背景连贯显示，打造沉浸式浏览体验。

ASO 规格对齐: 严格遵守 Apple 官方尺寸规范（6.7", 6.5" 等），一键导出全套素材。

🛠 技术架构 (Stack)
Frontend: Next.js 15+ (App Router) + Tailwind CSS

UI Components: Shadcn UI + Lucide React

Backend & Infrastructure: * Supabase Auth: 用户鉴权与个人库管理。

Supabase DB (PostgreSQL): 存储模板配置、文案记录与项目元数据。

Supabase Storage: 存储用户上传的原始截图 (Raw) 及生成的最终作品 (Export)。

Image Processing: Canvas API (结合 Fabric.js) 进行客户端实时渲染。

AI Orchestration: Gemini 1.5 Flash/Pro 用于视觉理解与文案本地化。

🤖 Claude Code 开发协议 (Prompt Context)
[!IMPORTANT]
当使用 Claude Code 辅助开发时，请严格遵守以下开发规范：

1. 状态管理与数据持久化
原则: 所有的样式配置（背景色、字体大小、样机型号）必须持久化在 Supabase 中，确保用户刷新页面后能继续编辑。

存储路径: 用户上传的图片统一存储在 storage/screenshots 路径下，采用 UUID/filename 命名。

2. UI/UX 准则
极简主义: UI 应参考 Apple 设计指南 (HIG)。避免过度拥挤，确保实时预览窗口（Live Preview）占据屏幕中心。

响应式: 预览组件必须支持缩放（Scale to Fit），确保在不同分辨率的屏幕下都能完整显示生成效果。

3. 性能优化
客户端处理: 复杂的 Canvas 绘图应在 Web Worker 中进行，避免阻塞主线程。

图片压缩: 在上传至 Supabase 之前，必须在客户端进行图片质量优化，减少带宽成本。

📅 路线图 (Roadmap)
[x] Milestone 1: MVP 框架 - 完成 Next.js + Supabase 基础环境搭建与图片上传。

[ ] Milestone 2: 模板引擎 - 实现 Telegram 风格渐变背景与 iPhone 15 Pro 样机嵌套。

[ ] Milestone 3: AI 文案介入 - 集成 Gemini API，实现根据截图自动填充 Header 文案。

[ ] Milestone 4: 导出系统 - 实现 Serverless Function 驱动的高清多尺寸打包下载。

🏁 快速开始指南
环境配置:

Bash
cp .env.example .env.local
# 填入你的 SUPABASE_URL, SUPABASE_ANON_KEY 和 GEMINI_API_KEY
安装依赖: npm install

运行开发环境: npm run dev

🎨 关于 Vibe 风格
本项目深度致敬 Telegram 的视觉语言：强调对比色、大字体标题、以及极其平滑的边框圆角。
