# VPS 剩余价值计算器 (VPS Residual Value Calculator)

一个专业级 VPS 剩余价值评估工具，支持多语言、多币种、国旗显示及精美卡片导出。

>  **项目来源**: 本项目基于 [Zen-iOS Design 的原始版本](https://qninq.cn/file/html/vpsrest/index.html) 进行二次开发与功能增强，在此表示感谢。

## ✨ 功能特性

- 🌐 **多语言支持**：自动根据浏览器语言切换中文/英文界面
- 🏳️ **国家/地区字段**：支持全球国家选择，高清国旗图标显示
- ️ **精美卡片导出**：一键生成 Zen-iOS 风格评估卡片 (WebP)
- 📝 **Markdown 导出**：支持导出完整评估报告，便于分享与存档
- 💱 **多币种汇率**：支持 CNY, USD, EUR, SGD, GBP, JPY, RUB 等实时汇率转换
- 📊 **灵活计算**：支持月付/季付/年付等多种订阅周期，可自定义溢价
- 📱 **响应式设计**：完美适配桌面端与移动端

## 🚀 在线部署

本项目为纯静态 HTML，可一键部署至任意静态托管平台：

### Cloudflare Pages (推荐)
1. Fork 本仓库到你的 GitHub 账号
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/) -> **Workers & Pages**
3. 点击 **Create application** -> **Pages** -> **Connect to Git**
4. 选择 `vpsrest` 仓库，分支选择 `master`
5. 保持默认构建设置（无需配置 Build Command）
6. 点击 **Save and Deploy**

部署成功后，你将获得一个免费的 `*.pages.dev` 域名。

### 本地运行
```bash
# 克隆仓库
git clone https://github.com/mouse0232/vpsrest.git
cd vpsrest

# 使用任意 HTTP 服务器启动
python3 -m http.server 8000
# 或使用 Node.js
npx serve .
```
访问 `http://localhost:8000` 即可使用。

## 🛠 技术栈

- **核心**：HTML5, React 18 (CDN), Babel Standalone
- **样式**：Tailwind CSS (CDN)
- **图标**：Lucide Icons (SVG)
- **二维码**：QRCode.js
- **国旗数据**：FlagCDN API + 本地国家列表

##  项目结构

```
vpsrest/
├── index.html          # 主程序入口 (单文件应用)
└── README.md           # 项目说明文档
```

## 📖 使用说明

1. **填写 VPS 信息**：输入名称、选择国家、填写配置参数
2. **设置财务信息**：选择订阅周期、输入价格与币种
3. **点击计算**：系统自动计算剩余价值并显示结果
4. **导出分享**：
   - 点击 **保存卡片**：下载高清 WebP 评估图片
   - 点击 **保存 MD**：下载 Markdown 格式评估报告

## 🌍 多语言支持

项目根据浏览器语言 (`navigator.language`) 自动切换：
- 中文环境：显示中文标签 (如"配置"、"总价值")
- 英文环境：显示英文标签 (如"CONFIGURATION"、"TOTAL VALUE")

如需强制切换语言，可在浏览器设置中更改首选语言。

## 📝 许可证

本项目仅供学习交流使用。

---

Made with ❤️ by Zen-iOS Design
