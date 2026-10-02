# PhoneTwin Studio

3D 手机产品演示工作台，由杨玄一设计并借助 AI 开发。

**[打开在线工作台](https://awoele.github.io/PhoneTwin-Studio/)**

- 3D 手机展示、视角调整与固定视角保存
- 动态背景与灯光预设
- 镜头预设、自定义运动轨迹及方案保存
- 10 种运镜、3 组成组编排；逐镜调整顺序、运动时长、停留与节奏
- 图片/视频导入与浏览器录制，录制时按 P 播放镜头
- 充电线、闪光和手势光尾展示效果

## 演示范围与隐私

此仓库存放 GitHub Pages 的生产发布文件、桌面软件发布与使用说明。
在线版不连接真机、不开放接收服务；导入媒体、镜头预设与录制在访客浏览器内处理。
真机画面与姿态同步通过本机版使用。手势光尾是工作台演示效果，不读取其他 iOS App 的触点。

## 下载安装

**电脑和 iPhone 需要配合使用，不是把整个工作台装到手机上。**

1. Windows 10/11（64 位）：从 [最新版本](https://github.com/awoele/PhoneTwin-Studio/releases/latest) 下载 `Setup-x64.exe` 安装版，或 `Portable-x64.exe` 免安装版。两者都包含运行环境，无需 Node、命令行或开发工具。
2. iPhone：先从 App Store 安装 TestFlight，再打开 [PhoneTwin Sender 邀请](https://testflight.apple.com/join/EFpEgJfW) 安装手机端。此入口由原项目维护者提供；本项目作者已确认可以安装，后续名额和有效期由原维护者控制。
3. 将电脑与 iPhone 连到同一 Wi-Fi；打开电脑端，接收服务会自动启动。首次出现 Windows 防火墙提示时，只为你信任的**专用网络**允许访问，不需要关闭防火墙。
4. 点击电脑工作台的连接图标 → **连接地址与二维码**；在 Sender 扫码，地址应为 `ws://电脑局域网IP:8788/native`，不能是 `localhost` 或 `127.0.0.1`。
5. 手机上允许本地网络、运动与健身及扫码所需相机权限，点击“准备 Sender 会话”；电脑点击“开始接收 iPhone”。
6. 手机上启动系统屏幕广播，选择 **PhoneTwin Broadcast**；首次将手机正面朝向自己，点击工作台校准图标。校准及镜头预设会保存在这台电脑上。

完整操作和排障见 [使用指南](docs/使用指南.md)。

### 使用边界

- 目前交付的是 **Windows x64 + iPhone Sender**，没有发布 macOS 或 Android 安装包。
- Windows 安装包尚未使用商业代码签名证书，系统可能显示“未知发布者”。请仅从本仓库 Releases 下载，并核对随版本提供的 SHA-256；不要关闭系统安全防护。
- 上游 TestFlight 版本只供非商用试用、技术演示、评估与反馈，不保证永久有效；这里提供原始邀请入口，不镜像或重新分发他人的 IPA。
- 手机投屏不是手机远程控制，任意 iOS App 的真实手指轨迹同步暂未支持。
- 手机需保持解锁并开启屏幕广播；无线延迟取决于 Wi-Fi、设备和屏幕内容。不把本地模拟测试等同于所有 iPhone/网络的真机验收。

## 来源与许可

- 开源基础：[ReinhartL/PhoneTwin-Studio](https://github.com/ReinhartL/PhoneTwin-Studio)，MIT，保留原始许可。
- 工作台设计与功能迭代：杨玄一，AI 辅助实现。
- 导演配方参考：[video-shotcraft](https://github.com/Vincentwei1021/video-shotcraft)（Apache-2.0），适配为实时 3D 手机运镜，不包含其 Remotion 引擎、音效资源或剪映导出功能。
- 手机模型：[Phone 17 Pro Max · Ranguel](https://sketchfab.com/3d-models/phone-17-pro-max-66809964eff043a39d553c3795995008)，[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)。已适配模型比例、动态屏幕纹理、材质及灯光。
- 模型、图片和第三方素材的权利归各自权利人；不以代码 MIT 许可替代素材许可。

## 发布

`main` 分支更新后，GitHub Actions 将 `site/` 发布到 GitHub Pages。
发布文件从本地工程以 `PHONETWIN_HTTP=1`、`VITE_PUBLIC_DEMO=1` 和 `--base=/PhoneTwin-Studio/` 构建。
