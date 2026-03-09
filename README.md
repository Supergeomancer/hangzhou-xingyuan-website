# 杭州兴元官网 - 网站部署指南

## 📁 文件夹结构说明

```
hangzhou_xingyuan_website/
├── index.html              # 网站首页文件
├── 兴元商务logo.jpg        # 品牌Logo图片
├── README.md               # 部署说明文档（本文件）
└── assets/                 # 资源文件夹（可选）
    └── images/             # 其他图片资源
```

## 🚀 快速部署方法

### 方法一：本地部署
1. 将 `hangzhou_xingyuan_website` 文件夹复制到你的Web服务器根目录
2. 使用浏览器访问 `http://your-domain.com/` 或 `http://localhost/`

### 方法二：使用Python简易服务器
在文件夹内打开终端，执行：
```bash
python -m http.server 8000
```
然后在浏览器访问：`http://localhost:8000`

### 方法三：使用Node.js的http-server
```bash
# 安装
npm install -g http-server

# 运行
http-server -p 8000
```
然后访问：`http://localhost:8000`

## 🌐 云服务器部署

### 阿里云/腾讯云/AWS等
1. 将整个文件夹上传到服务器的 `/var/www/html/` 或指定目录
2. 确保Nginx或Apache配置正确指向该目录
3. 重启Web服务器

### Nginx配置示例
```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/html/hangzhou_xingyuan_website;
    index index.html;

    location / {
        try_files $uri $uri/ /index.html;
    }
}
```

## 📦 静态网站托管平台

### Vercel（推荐）
```bash
# 安装Vercel CLI
npm i -g vercel

# 部署
vercel
```

### Netlify
```bash
# 安装Netlify CLI
npm install -g netlify-cli

# 部署
netlify deploy --prod
```

### GitHub Pages
1. 创建GitHub仓库
2. 上传 `hangzhou_xingyuan_website` 文件夹内容
3. 在仓库Settings中启用GitHub Pages
4. 访问 `https://your-username.github.io/repository-name/`

## 🔧 网站配置说明

### 页面信息
- **标题**：杭州兴元未来信息科技有限公司 - 元宇宙内容生态引领者
- **语言**：中文（zh-CN）
- **响应式设计**：支持桌面端和移动端

### 浏览器兼容性
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📞 技术支持

如遇部署问题，请检查：
1. 文件路径是否正确
2. 图片文件 `兴元商务logo.jpg` 是否存在
3. Web服务器配置是否正确
4. 防火墙端口是否开放（默认80/443端口）

## 📄 版权信息

© 2025 杭州兴元未来信息科技有限公司 版权所有

---

**生成时间**：2025年3月9日
