# 心语 AI（Android Studio 原型）

## 当前包含
- Kotlin + Jetpack Compose 应用界面
- 可配置的 DeepSeek / OpenAI 兼容 Chat Completions API
- 本机保存 API 配置
- 打开 Android 无障碍设置的入口
- 微信前台应用检测原型（不读取消息、不自动发送）

## 当前不包含
为了避免误发消息，当前原型**不会读取微信聊天内容、不会自动点击发送，也不是已验证可用的微信自动回复器**。微信界面识别与自动发送需要在目标手机和微信版本上单独验证，并加入去重、敏感内容拦截、发送确认和紧急停止机制。

## 环境
- Android Studio
- JDK 17
- Android SDK 35
- Gradle 8.9 或与 Android Gradle Plugin 8.7.3 兼容的 Gradle

## 构建 APK
1. 解压项目，在 Android Studio 中打开 `XinyuAI` 文件夹。
2. 等待 Gradle Sync 完成。
3. 选择 Build > Build APK(s)。
4. APK 通常输出到 `app/build/outputs/apk/debug/app-debug.apk`。

也可在安装了 JDK 与 Android SDK 的环境中执行：
`gradle assembleDebug`

## 配置 API
默认示例使用 `https://api.deepseek.com` 和 `deepseek-chat`。请在应用内填写自己的 API Key。模型名称与接口地址以服务商当前文档为准。不要将含有真实 API Key 的 APK 发给别人；正式产品应通过自己的 HTTPS 服务端代理调用模型，避免密钥被提取。

## Android 无障碍
用户需在系统设置中主动开启服务。请仅在本人设备、本人账号和获得聊天参与者适当授权的范围内使用。遵守微信相关规则，不要用于批量骚扰、冒充真人或发送验证码、支付等敏感内容。
