# 🏛️ 智慧图书馆管理系统

一个基于微信小程序的现代化图书借阅管理系统，采用前后端分离架构，包含用户端小程序、后台管理系统和REST API服务。
![Uploading image.png…]()


> 🎯 **基于 [Vue Element Admin](https://panjiachen.github.io/vue-element-admin-site/zh/) 官方最佳实践构建**

[![Vue](https://img.shields.io/badge/Vue-2.6.10-brightgreen.svg)](https://vuejs.org/)
[![Element UI](https://img.shields.io/badge/Element%20UI-2.13.2-brightgreen.svg)](https://element.eleme.io/)
[![ThinkPHP](https://img.shields.io/badge/ThinkPHP-6.1.4-orange.svg)](https://www.thinkphp.cn/)
[![UniApp](https://img.shields.io/badge/UniApp-Vue3-blue.svg)](https://uniapp.dcloud.io/)

## 项目结构

```
tsxcx/
├── kaogong.bzyun.club/          # 后端API (ThinkPHP 6.1.4)
├── tushu/                       # 小程序前端 (UniApp + Vue 3)
├── vue-element-admin-master/    # 后台管理系统 (Vue + Element UI)
└── README.md                    # 项目说明文档
```

## 技术栈

### 后端
- **框架**: ThinkPHP 6.1.4
- **数据库**: MySQL 5.6
- **认证**: JWT Token
- **API**: RESTful API

### 小程序前端
- **框架**: UniApp
- **语言**: Vue 3 + JavaScript
- **UI**: 原生小程序组件
- **平台**: 支持微信小程序、支付宝小程序等

### 后台管理系统
- **框架**: Vue 2.6 + Element UI 2.13
- **构建工具**: Vue CLI
- **图表**: ECharts
- **状态管理**: Vuex

## 核心功能

### 用户端小程序
- 🔐 **用户认证**: 微信授权登录、手机号登录
- 📚 **图书浏览**: 图书搜索、分类筛选、详情查看
- 📱 **扫码借阅**: 相机扫描条形码快速借阅
- 🛒 **在线选书**: 在线浏览并借阅图书
- 📖 **借阅管理**: 查看借阅记录、归还提醒
- 📅 **图书预约**: 预约暂时无库存的图书
- 👑 **会员服务**: 会员等级、权益管理
- 💳 **订单管理**: 会员开通、罚金缴费
- ⭐ **图书评价**: 评分评价系统
- 🔔 **消息通知**: 借阅提醒、归还通知

### 后台管理系统
- 📊 **数据看板**: 借阅统计、用户分析、趋势图表
- 📚 **图书管理**: 图书信息管理、分类管理、库存管理
- 👥 **用户管理**: 用户信息、会员管理、信用管理
- 📋 **借阅管理**: 借阅记录、超期处理、强制归还
- 💰 **订单管理**: 订单查询、退款处理
- 📈 **统计分析**: 多维度数据分析、报表导出
- ⚙️ **系统设置**: 参数配置、权限管理

## 数据库设计

系统包含16个核心数据表：

- **用户相关**: users, user_memberships, membership_levels
- **图书相关**: books, authors, categories, book_copies
- **借阅相关**: borrow_records, reservations, reviews
- **订单相关**: orders, coupons, user_coupons
- **系统相关**: admins, notifications, system_settings

## 快速开始

### 1. 环境要求

- PHP >= 7.2.5
- MySQL >= 5.6
- Node.js >= 12
- Composer
- HBuilderX (用于UniApp开发)

### 2. 后端部署

```bash
# 进入后端目录
cd kaogong.bzyun.club

# 安装依赖
composer install

# 配置环境
cp .env.example .env
# 编辑.env文件，配置数据库连接信息

# 导入数据库
mysql -u username -p database_name < database/migrations/create_tables.sql

# 启动服务
php think run
```

### 3. 小程序部署

```bash
# 进入小程序目录
cd tushu

# 用HBuilderX打开项目
# 配置AppID和服务器域名
# 编译并发布到微信小程序
```

### 4. 后台管理系统部署

```bash
# 进入后台管理系统目录
cd vue-element-admin-master

# 安装依赖
npm install

# 配置API地址
# 编辑.env.development和.env.production文件

# 开发模式
npm run dev

# 生产构建
npm run build:prod
```

## 部署配置

### 服务器配置

1. **Web服务器**: Nginx/Apache
2. **PHP配置**: 启用相关扩展
3. **数据库**: MySQL 5.6+
4. **SSL证书**: HTTPS配置（小程序要求）

### 微信小程序配置

1. 在微信公众平台注册小程序
2. 配置服务器域名白名单
3. 设置支付功能（如需要）
4. 配置扫码权限

### 安全配置

- JWT密钥配置
- 数据库连接加密
- API接口安全防护
- 文件上传安全限制

## 开发指南

### 后端开发

- 遵循ThinkPHP规范
- 使用Model-Controller架构
- 统一API返回格式
- 完善的错误处理

### 前端开发

- 遵循Vue最佳实践
- 组件化开发
- 响应式设计
- 用户体验优化

### 代码规范

- PSR-4自动加载标准
- ESLint代码检查
- 统一的命名规范
- 完整的注释文档

## 贡献指南

1. Fork 本项目
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 许可证

本项目采用 MIT 许可证。详细信息请查看 [LICENSE](LICENSE) 文件。

## 联系方式

如有问题或建议，请通过以下方式联系：
微信：jwl059969

## 更新日志

### v1.0.0 (2025-01-08)
- ✨ 初始版本发布
- 🔐 用户认证系统
- 📚 图书管理功能
- 📱 扫码借阅功能
- 👑 会员管理系统
- 📊 数据统计分析
- 🎨 现代化UI设计

---

**智慧图书馆管理系统** - 让阅读更智能，让管理更简单
