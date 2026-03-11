# ☕ 咖啡学院 - Cloudflare Pages 部署指南

## 🚀 快速部署（5 分钟完成）

### 第一步：获取 Cloudflare API Token

1. 访问 [Cloudflare Dashboard](https://dash.cloudflare.com)
2. 登录或注册账号（免费）
3. 点击右上角头像 → **My Profile**
4. 选择 **API Tokens** 标签
5. 点击 **Create Token**
6. 选择 **Edit Cloudflare Workers** 模板（或自定义）
7. 权限设置：
   - **Account.Cloudflare Pages** → **Edit**
   - **Account.Workers and Pages** → **Edit**
8. 点击 **Continue to summary**
9. 点击 **Create Token**
10. **复制 Token**（只显示一次，保存好！）

### 第二步：本地部署

打开命令行，运行：

```bash
# 设置 API Token（替换为你的实际 Token）
set CLOUDFLARE_API_TOKEN=你的 API_TOKEN_在这里

# 进入项目目录
cd C:\Users\52014\.openclaw\workspace\咖啡教学网站

# 部署到 Cloudflare Pages
wrangler pages deploy . --project-name=coffee-academy
```

### 第三步：完成！

部署成功后，你会看到类似输出：
```
✨ Deployment complete!
Your site is now live at: https://coffee-academy.pages.dev
```

🎉 现在任何人都可以访问这个链接，无需密码！

---

## 📋 替代方案：通过 GitHub 部署（无需 API Token）

如果不想用 API Token，可以用 GitHub 方式：

### 步骤：

1. **创建 GitHub 仓库**
   - 访问 [github.com/new](https://github.com/new)
   - 仓库名：`coffee-academy`
   - 设为公开（Public）

2. **上传网站文件**
   ```bash
   cd C:\Users\52014\.openclaw\workspace\咖啡教学网站
   git init
   git add .
   git commit -m "☕ 咖啡学院初始版本"
   git branch -M main
   git remote add origin https://github.com/你的用户名/coffee-academy.git
   git push -u origin main
   ```

3. **连接 Cloudflare Pages**
   - 访问 [pages.cloudflare.com](https://pages.cloudflare.com)
   - 点击 **Create a project**
   - 选择 **Connect to Git**
   - 选择你的 `coffee-academy` 仓库
   - 点击 **Begin setup**
   - 项目名：`coffee-academy`
   - 点击 **Save and Deploy**

4. **完成！**
   - 等待 1-2 分钟构建
   - 获得永久链接：`https://coffee-academy.pages.dev`

---

## 🎯 自定义域名（可选）

部署完成后，可以绑定自己的域名：

1. 在 Cloudflare Pages 项目设置中
2. 选择 **Custom domains**
3. 点击 **Add custom domain**
4. 输入你的域名（如 `coffee.yourdomain.com`）
5. 按提示配置 DNS

---

## 📊 部署信息

| 项目 | 值 |
|------|-----|
| **项目名** | coffee-academy |
| **框架** | 静态 HTML |
| **构建命令** | 无需构建 |
| **输出目录** | 根目录 `/` |
| **免费额度** | 无限带宽 |

---

## ✅ 部署后检查清单

- [ ] 网站可以正常访问
- [ ] 所有页面链接正常
- [ ] 图片和样式加载正确
- [ ] 移动端显示正常
- [ ] 分享链接给朋友测试

---

## 🔗 你的网站

**部署后的链接格式：**
```
https://coffee-academy.pages.dev
```

或自定义域名：
```
https://你的域名.com
```

---

## 💡 提示

- Cloudflare Pages 完全免费，适合个人项目
- 自动 HTTPS，无需配置证书
- 全球 CDN 加速，访问速度快
- 支持自动部署（连接 GitHub 后，每次 push 自动更新）

---

*准备好了吗？开始部署吧！☕🚀*
