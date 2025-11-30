# Run Time Adder Script 使用说明

本项目支持两种登录方式来访问 **Pterodactyl** 或相关系统：

1. **使用 Cookie 登录**  
2. **使用邮箱和密码登录**

---

## 方式一：使用 Cookie 登录

### 适用场景
- 需要保持长期会话，避免频繁登录。
- 已经拥有有效的 Cookie，可以直接复用。

### 获取 Cookie 的步骤
1. 登录目标网站（如 **Pterodactyl** 面板）。
2. 打开浏览器 **开发者工具**（按 `F12` 或右键点击页面选择 **检查**）。
3. 切换到 **Application（应用）** 标签页。
4. 在左侧找到 **Cookies** 部分，选择当前网站。
5. 找到与登录相关的 cookie（例如 `session`, `auth_token` 等）。
6. 复制该 Cookie 值。

### 在 GitHub Secrets 中配置
1. 打开 GitHub 仓库，进入 **Settings > Secrets and variables > Actions**。
2. 点击 **New repository secret**。
3. 新建一个名为 `REMEMBER_WEB_COOKIE` 的 secret，并将复制的 Cookie 值粘贴进去。

### 好处
- 每次工作流运行时会自动使用该 Cookie 进行登录，无需再次输入账号和密码。

---

## 方式二：使用邮箱和密码登录

如果没有有效的 Cookie，可以使用邮箱和密码方式登录。

### 在 GitHub Secrets 中配置
1. 打开 GitHub 仓库，进入 **Settings > Secrets and variables > Actions**。
2. 点击 **New repository secret**。
3. 新建以下两个 Secrets：
   - `PTERODACTYL_EMAIL`：你的 Pterodactyl 账户邮箱。
   - `PTERODACTYL_PASSWORD`：你的 Pterodactyl 账户密码。

### 好处
- 无需手动获取 Cookie，直接用账号信息完成登录。

---

## 推荐做法
- **优先使用 Cookie**：稳定性更高，不会因为密码变动导致任务失败。  
- **备用邮箱/密码方式**：当 Cookie 失效时，可以使用邮箱和密码重新登录。  

---
