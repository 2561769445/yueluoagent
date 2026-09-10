# YueluoAgent

> 月落 Agent — 本地优先的自托管 AI Agent(TypeScript + SQLite 重写,融合 pi / hermes-agent / ZCode 三家精华)

## ⚠️ 免责声明 / Disclaimer

**本项目仅供学习、研究及合法授权范围内的技术测试使用。**

- 使用者**必须遵守所在国家及地区的法律法规**,包括但不限于《中华人民共和国网络安全法》《中华人民共和国刑法》(第二百八十五条、第二百八十六条)等相关规定
- **严禁**将本项目用于任何违法犯罪活动,包括但不限于:未经授权的网络入侵、攻击他人信息系统、窃取公民个人信息、传播木马病毒、破坏计算机数据等
- 因下载、使用或传播本项目而产生的一切后果与法律责任,**由使用者本人独立承担**,与本项目作者及贡献者无关
- 如果不同意本声明,请立即删除并停止使用本项目

**This project is for educational and research purposes ONLY. Users MUST comply with all applicable local laws and regulations. Any ILLEGAL use of this software is strictly PROHIBITED. Users assume full legal responsibility for their own actions. If you do not agree, delete this project immediately.**

## 📦 下载

直接下载仓库中的 `YueluoAgent-v1.0.zip`(约 35MB,解压即用)。

## 🚀 启动

**Windows(最简单):**

```bat
解压后双击「启动月落.bat」
```

**手动启动(Windows / Linux 通用):**

```bash
unzip YueluoAgent-v1.0.zip
cd yueluo-agent
npm install        # 首次需要,仅 playwright-core 一个依赖;包内已带 node_modules 时可跳过
node yueluo.ts     # Node 24+ 原生运行 .ts
```

- 启动后自动打开 **http://127.0.0.1:8765**
- 已预配置 **DeepSeek**(deepseek-chat);换模型/供应商点右上「设置」(内置 31 个供应商预设 + 本地 Ollama/LM Studio)
- 没有 API key?选「月落测试模型」preset,即可验证全链路

**手机远程控制:**

1. 启动后点侧栏「📱 手机控制」→ 弹出二维码(携带访问令牌,扫码直达)
2. 手机扫码(或输入局域网地址 + 8 位配对码)→ 远程对话、远程执行命令、审批命令,多端实时同步
3 手机连不上时放行防火墙:`netsh advfirewall firewall add rule name="YueluoAgent" dir=in action=allow protocol=TCP localport=8765`

> ⚠️ 拿到令牌/配对码的人都能在这台电脑上执行命令,勿外传;公网部署请自加反向代理与强认证。

## ✨ 主要能力

- **Web 控制台**: SSH / RDP / Cron 定时任务 / 群组会话 / 内置浏览器自动化(Playwright)
- **多 LLM 供应商**: 31 个预设(OpenAI/DeepSeek/Anthropic/Gemini/xAI/MiniMax…)+ 本地模型 + 自定义端点,六种 API 模式
- **会话树 / 子代理 / 后台任务**: 会话分叉分支切换、delegate_task 隔离委派、spawn_background 并行
- **SKILL.md 技能系统**: agentskills.io 标准,兼容 pi 与 hermes 技能库
- **SQLite + FTS5 中文全文搜索**,自动上下文压缩
- **PWA**: 手机添加到主屏,像原生 App

更多细节见压缩包内的完整 README。

## License

仅供学习研究使用。
