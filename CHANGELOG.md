# Changelog

## [0.2.2] - 2026-09-13

### Fixed

- integration: 设备实体注册回归——推送开关首次刷新改为限时/后台，避免阻塞 entry setup 超时回滚
- addon: 消除 bridge segfault（去掉 chroot/mount，直接 bionic linker 运行）
- addon: 剔除 bridge 开头的 type-0 垃圾 NAL，修复 RTSP 无画面
- addon: v8 末帧保持代理 repeater.py——相机间歇停推时循环重放 GOP，RTSP 不掉线、HA 不黑屏
- integration: 云端录像时间戳防御性归一化

### Changed

- addon 镜像 tag 修正 + README addon 安装章节

## [0.2.1] - 2026-07-11

- 影腾智联 HA 集成全功能复刻：直播 / PTZ / 云录像 / 告警 / 设备设置 / SD 回放 / 共享 / 双向语音
- addon 化：tengying_bridge 移到仓库根，使用 ghcr image 字段（Supervisor 面板一键安装）
