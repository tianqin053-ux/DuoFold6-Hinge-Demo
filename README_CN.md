# DuoFold6Demo

这是一个针对 Samsung Galaxy Z Fold6（SM-F9560 / Android 16）的“iPhone Duo 风格连续展开”桌面原型。

## 当前版本能做什么
- 使用 Android `TYPE_HINGE_ANGLE` 读取铰链角度。
- 0°→180° 时连续计算动画进度。
- 时钟、天气卡片、图标、Dock 和背景按同一进度做位置/尺寸/透明度变化。
- 作为 Launcher/Home Activity，可设置为默认桌面。
- 不需要 Root，不需要刷机，不会清除手机数据。

## 重要说明
这是第一版视觉 Demo，不是 One UI 的系统级替换，因此不能让微信、抖音等第三方 App 内部控件跟着铰链角度连续形变。

## 用 Android Studio 构建
1. Android Studio 打开本项目目录 `DuoFold6Demo`。
2. 等 Gradle Sync 完成。
3. 连接 Fold6，开启“开发者选项/USB 调试”。
4. Run `app`。
5. 第一次打开后，按系统提示将 “Duo Fold 6 Demo” 设为默认主屏即可体验。

如果你只想临时体验，不设默认桌面也可以直接运行 Activity。

## 下一版建议
- 使用真实壁纸并做“连续裁剪/视差”。
- 增加真实 App 图标与点击启动。
- 根据 Fold6 实际内外屏尺寸做逐像素标定。
- 增加折叠→半开→完全展开的非线性运动曲线，进一步贴近你提供的视频。
- 可选加入 AndroidX WindowManager，处理折叠状态、遮挡区域和大屏布局。
