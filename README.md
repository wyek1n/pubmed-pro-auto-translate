# Pubmed.pro 自动翻译脚本

一个用于在 Pubmed.pro 网站上自动点击所有英汉翻译按钮的油猴脚本（Tampermonkey/Greasemonkey）。

## 📝 功能描述

该脚本可以在访问 Pubmed.pro 网站时自动激活所有论文的英汉翻译功能，无需手动逐个点击翻译按钮。

## ✨ 特性

- 🔄 **自动识别翻译按钮**：使用多种CSS选择器精准定位翻译开关
- 🚫 **防重复点击**：智能检测按钮状态，避免重复操作
- 👀 **动态内容监听**：实时监听页面变化，处理异步加载的内容
- ⏰ **定期检查**：每5秒自动检查新出现的翻译按钮
- 📱 **兼容性好**：支持 Tampermonkey 和 Greasemonkey

## 🚀 安装使用

### 1. 安装用户脚本管理器
- [Tampermonkey](https://www.tampermonkey.net/) (推荐)
- [Greasemonkey](https://www.greasespot.net/) (Firefox)

### 2. 安装脚本
1. 点击 [pubmed_pro_auto_translate.user.js](./pubmed_pro_auto_translate.user.js) 下载脚本文件
2. 复制脚本内容到用户脚本管理器中
3. 保存并启用脚本

### 3. 使用
访问 [Pubmed.pro](https://www.pubmed.pro/) 网站进行论文检索，脚本将自动运行并激活翻译功能。

## 🎯 测试网址

可以在以下网址测试脚本效果：
```
https://www.pubmed.pro/search/中医药大模型?content=2&iFactor=0,7&threshold=0.8
```

## 🔧 技术细节

### 目标元素选择器
脚本支持多种选择器来确保兼容性：
- `span.el-switch__core[style*="width: 40px"]`
- `#pane-pubmed span.el-switch__core`
- `.articleList span.el-switch__core`
- `.translate span.el-switch__core`

### 执行时机
- 页面加载完成后延迟2秒执行
- 监听DOM变化，处理动态加载内容
- 每5秒进行一次检查

## 🐛 问题反馈

如果遇到问题或有改进建议，请创建 Issue。

## 📄 许可证

本项目采用 MIT 许可证。

## 📊 版本历史

- v1.0 - 初始版本，支持自动点击翻译按钮
