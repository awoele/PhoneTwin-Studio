# PhoneTwin Studio

3D 手机产品演示工作台，由杨玄一设计并借助 AI 开发。

**[打开在线工作台](https://awoele.github.io/PhoneTwin-Studio/)**

- 3D 手机展示、视角调整与固定视角保存
- 动态背景与灯光预设
- 镜头预设、自定义运动轨迹及方案保存
- 图片/视频导入与浏览器录制，录制时按 P 播放镜头
- 充电线、闪光和手势光尾展示效果

## 演示范围与隐私

此仓库存放 GitHub Pages 的生产发布文件。完整开发工程保留在本地。
在线版不连接真机、不开放接收服务；导入媒体、镜头预设与录制在访客浏览器内处理。
真机画面与姿态同步通过本机版使用。手势光尾是工作台演示效果，不读取其他 iOS App 的触点。

## 来源与许可

- 开源基础：[ReinhartL/PhoneTwin-Studio](https://github.com/ReinhartL/PhoneTwin-Studio)，MIT，保留原始许可。
- 工作台设计与功能迭代：杨玄一，AI 辅助实现。
- 手机模型：[Phone 17 Pro Max · Ranguel](https://sketchfab.com/3d-models/phone-17-pro-max-66809964eff043a39d553c3795995008)，[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)。已适配模型比例、动态屏幕纹理、材质及灯光。
- 模型、图片和第三方素材的权利归各自权利人；不以代码 MIT 许可替代素材许可。

## 发布

`main` 分支更新后，GitHub Actions 将 `site/` 发布到 GitHub Pages。
发布文件从本地工程以 `PHONETWIN_HTTP=1`、`VITE_PUBLIC_DEMO=1` 和 `--base=/PhoneTwin-Studio/` 构建。
