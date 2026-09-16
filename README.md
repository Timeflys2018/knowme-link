# knowme-link

KnowMe 深链接跳板（GitHub Pages，零服务器）。

- `/join/#<token>` — 读 hash 里的 base64url token，跳转 `knowme://join/<token>` 唤起已安装的 KnowMe 加入共享空间；未安装则引导下载。纯静态、无服务端、无付费风险。
- token 逐字透传给系统（不在此解码/执行）。内容明文存于 git 远端、非端到端加密；权限由 git 平台管理。

方案 C（见 zhiwo DECISIONS SYNC-D15）：微信/飞书只认 https，自定义 scheme 不可点，故用一个可点的 https 静态页做 302/JS 跳板到 knowme://。
