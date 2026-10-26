# knock-knock

面向移动开发者的推送测试工具箱，基于 [FCM-toolbox](https://github.com/SimonMarquis/FCM-toolbox) 派生，参考 [DooPush](https://github.com/doopush/doopush) 的多通道适配方案。目标采用 Kotlin Multiplatform（KMP）与 Compose Multiplatform（CMP），覆盖 Android 和 iOS，只测试工具箱自身安装实例的各通道收发。

> 当前处于设计阶段：已创建 Fork 并形成开发文档；KMP/CMP、iOS 和国内厂商通道改造尚未实施。现有应用与 Firebase 代码来自上游，不代表 knock-knock 的目标功能已经可用。

## 开发文档

| 文档 | 内容 |
|---|---|
| [项目设计](docs/design.md) | 产品边界、架构取舍、平台能力、数据契约、接口及验收不变量 |
| [开发与验收计划](docs/development-plan.md) | 任务依赖、阶段范围、实施门槛、验证要求及当前交接状态 |

先阅读项目设计，再按开发计划评审架构、冻结工具链和落实平台账号，之后进入代码实施。首版拟覆盖 Android FCM、iOS FCM/APNs，国内厂商通道分阶段接入；具体范围以设计文档为准。

## 当前仓库

- `app/`：上游 Android 应用。
- `firebase/`：上游 Firebase Functions 与 Web 应用。
- `docs/design.md`、`docs/development-plan.md`：knock-knock 开发文档。
- `docs/index.html`：上游网页资产，保留原用途。

`shared/`、`iosApp/`、独立发送服务和新 Web 控制台属于拟议改造，尚未创建。上游商店链接、公开演示服务及 Firebase 配置均不作为 knock-knock 的发布或测试入口；独立应用身份和服务配置要求见项目设计。

## 来源与许可

- 本仓库：[tipsypotato/knock-knock](https://github.com/tipsypotato/knock-knock)，对应 Git 远端 `origin`。
- 父仓：[SimonMarquis/FCM-toolbox](https://github.com/SimonMarquis/FCM-toolbox)，对应 Git 远端 `upstream`。
- 初始研究与分叉基线：`f793400b65f038b408dd04a73cdb10334ed87886`；[上游原始说明](https://github.com/SimonMarquis/FCM-toolbox/blob/f793400b65f038b408dd04a73cdb10334ed87886/README.md)保留安装、截图与原实现参考。
- 保留上游 [Apache-2.0 许可证](LICENSE)。DooPush 目前仅作为调研参考，后续若复制代码，需按开发文档保留其 MIT 声明并记录来源。
