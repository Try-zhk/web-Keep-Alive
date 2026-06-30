# 🔔 Keep Alive

自动定时 ping 服务，防止 Hugging Face Space / Render / Railway 等平台休眠。

## 快速开始

### 1. Fork 本仓库

### 2. 添加 Secret

进入仓库 → **Settings → Secrets and variables → Actions → New repository secret**

| Secret 名称 | 示例值 |
|------------|--------|
| `KEEPALIVE_URLS` | `https://mvurl-my-mc-bot.hf.space/,https://your-other-service.com` |

多个 URL 用英文逗号 `,` 分隔。

### 3. 启用 Actions

进入 **Actions** 标签页，点击 **Enable workflows**。

### 4. 完成

每 5 分钟自动 ping 一次，冷启动超时设为 30 秒，不会误判 Down。

---

## 支持平台

- Hugging Face Space（免费版）
- Render 免费实例
- Railway 休眠服务
- 任何 HTTP/HTTPS 服务

## 注意事项

- GitHub Actions 免费版每月有 2000 分钟额度，每 5 分钟跑一次约消耗 **288 分钟/天**，注意用量
- 如需节省额度，可改为每 10 分钟：`*/10 * * * *`
- HF Space 冷启动一般 10~20 秒，30 秒超时足够
