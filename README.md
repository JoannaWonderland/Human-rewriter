# 人话改写器

把带「AI 腔 / 翻译腔 / 套话感」的中文，改写成更自然、平实、像人说的话。

这是一个纯前端 Web 小工具。你可以直接打开 `index.html` 使用，也可以部署到 GitHub Pages。

## 功能

- 实时检测常见 AI 味：套话、破折号堆砌、句子长短过于均匀、虚动词等。
- 支持两种改写风格：平实、犀利白话。
- 支持轻度 / 中度 / 重度三档改写强度。
- 使用 OpenRouter 调用大模型，支持预设模型和自定义 model slug。
- 长文会自动分段处理，并流式显示结果。
- API key 只保存在当前浏览器的 `localStorage` 里。

## 快速使用

1. 打开 `index.html`。
2. 填入你的 OpenRouter API key。
3. 粘贴要改写的文字。
4. 选择风格和强度。
5. 点击「改成人话」。

## 部署到 GitHub Pages

GitHub Pages 是 GitHub 提供的静态网站托管服务。静态网站指的是只靠 HTML、CSS、JavaScript 运行的网站，不需要后端服务器。

推荐流程：

1. 在 GitHub 新建一个仓库，比如 `renhua-rewriter`。
2. 把本项目里的文件推送到仓库。
3. 进入仓库的 `Settings` -> `Pages`。
4. Source 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`。
6. 保存后等待 GitHub 生成访问链接。

## OpenRouter API key

API key 可以理解成调用模型服务的「钥匙」。这个工具采用 BYOK 模式，也就是 Bring Your Own Key，用户自己填自己的 key，费用也由自己的 OpenRouter 账号承担。

获取方式：

- 打开 <https://openrouter.ai/keys>
- 登录后创建 key
- 复制到工具顶部的输入框

## 隐私说明

- AI 味检测在浏览器本地运行，不会上传。
- 改写时，原文会发送给 OpenRouter 和你选择的模型提供方。
- API key 会保存到当前浏览器的 `localStorage`，不会提交到本仓库，也不会发给作者。
- 不要把自己的 API key 写进代码、README、issue、截图或提交记录里。

## 本地开发

这个项目目前是单文件静态应用，不需要构建步骤。

如果你想用本地服务器预览，可以运行：

```bash
python3 -m http.server 5173
```

然后打开：

```text
http://localhost:5173
```

`localhost` 是你自己电脑上的本地地址，只能在本机访问。

## 许可证

MIT
