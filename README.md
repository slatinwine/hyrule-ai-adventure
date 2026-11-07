# 海拉鲁大陆冒险 · AI 主理人

一款中文文字冒险游戏：跟随公主修习魔法、跟随林克成为勇者、投靠加农毁灭海拉鲁，或谁都不跟，自由经商、觐见国王、倒卖武器、探险寻宝。剧情由云端 AI 主理人实时生成。

## 正式链接

**https://hyrule-ai-adventure.app.workbuddy.host/?sharecode=G3TH3EVURF**

本仓库的 GitHub Pages 站点 `https://slatinwine.github.io/hyrule-ai-adventure/` 是**镜像指引页**，打开后会跳转到上面的正式链接。

原因是 AI 主理人通过 WorkBuddy Cloud Service 调用云端大模型，服务端会校验请求来源（Origin）。只有在正式应用域名下，云端鉴权与流式生成才能正常工作；把游戏本体直接放在 GitHub Pages 上会无法生成剧情。因此这里保留一个轻量跳转页，避免分享出去的链接是坏掉的。

跳转页支持 `?stay=1` 参数停在镜像页不跳转，也可以点「留在此页」。

## 仓库内容

| 路径 | 说明 |
| --- | --- |
| `index.html` | GitHub Pages 入口，5 秒自动跳转正式链接，附「留在此页」与离线版入口 |
| `classic.html` | 离线剧本版，无需联网与登录，四条路线、魔法装备、商店委托、七张场景插画、完整结局 |
| `images/*.webp` | 七张统一画风的场景插画（复古绘本 / 鼠尾草绿 / 古金 / 羊皮纸） |
| `.nojekyll` | 让 GitHub Pages 原样发布静态文件 |

离线剧本版可直接访问 `https://slatinwine.github.io/hyrule-ai-adventure/classic.html`。插画已内嵌进 HTML，即使不带 `images/` 目录也能显示。

## 关于正式版

正式版是单文件 Web 云应用，包含：

- AI 主理人实时生成剧情，结构化 JSON 协议 + 前端白名单校验与转义
- 直连 Flash 快模型（`deepseek-v4.1-flash` 等），约 2.6–3.1 秒生成一轮
- Email OTP 登录、按账号隔离的云存档、本机存档、场景图鉴
- 七处著名场景，抵达时自动触发对应插画

AI 版源码不在本仓库：它依赖应用专属的云端配置，放在公开仓库里既无法运行也没有意义。

## 关注公众号

![公众号二维码](qrcode.jpg)
