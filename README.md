# Vercel Site Info API

轻量级网站信息获取接口服务，可快速部署至Vercel平台

## 功能特性

- 实时获取网站基础信息
- 简易API调用方式
- Vercel一键部署
- 多域名安全校验

## 快速部署

### Vercel 部署指南

1. **Fork仓库**  
   [点击fork按钮](https://github.com/YShenZe/vercel-site-info-api/fork) 将此项目复制到你的账户

2. **创建Vercel项目**  
   [前往Vercel控制台](https://vercel.com/new) 导入fork后的仓库

3. **配置环境变量**  
   在项目设置 > Environment Variables 添加：

   | 变量名 | 示例值 | 说明 |
   |-------|--------|-----|
   | HOSTS | `['', 'localhost', 'yourdomain.com']` | 允许访问的域名列表 |

> [!TIP]
> - 空值(`''`)允许直接访问  
> - `localhost`保留用于本地测试  
> - 将`yourdomain.com`替换为你的实际域名


## 使用方法

### API调用示例

```bash
GET https://your-api-domain.com/api/v1/?url=https://example.com
```

### Stellar主题集成

在主题配置文件中添加：

```yaml
api: https://your-api-domain.com/api/v1/?url=${href}
```

## 注意事项

- 生产环境建议移除`localhost`配置
- 多个域名请用英文逗号分隔
- API响应包含CORS头信息，支持跨域调用
- 默认无请求频率限制，如需限制可在Vercel配置速率规则

---

> 项目基于MIT协议开源，欢迎提交PR改进项目 [查看源码](https://github.com/YShenZe/vercel-site-info-api)