# CnMathTaxonomy Pages

中小学知识图谱（CnMathTaxonomy）的 GitHub Pages 静态页面仓库，用于托管隐私政策和用户协议，供 HarmonyOS 应用市场上架审核使用。

## 应用信息

- 应用名称：中小学知识图谱（CnMathTaxonomy）
- 包名：com.xmgod.cnmathtaxonomy
- 版本：1.0.0
- 平台：HarmonyOS（API 26 / HarmonyOS 6.0.0(20)+）
- 应用源码仓库（Gitee）：git@gitee.com:kuku-harmonyos/cn-math-taxonomy.git
- 内置数据来源：开源项目 cn-math-taxonomy，CC BY-NC 4.0 许可

## 关键合规事实

页面正文与下列实现事实一一对应，修改应用时需同步核对：

- `entry/src/main/module.json5` 未声明任何 `requestPermissions`，包括网络权限；应用完全离线运行。
- 学习数据（诊断会话、逐题作答、错题、收藏、偏好设置）存放在应用沙箱内的本地 SQLite 数据库与 preferences 文件，未加密、不上云。
- 备份导出/导入使用系统 `DocumentViewPicker`，导入为全量覆盖。
- 相册写入仅在诊断报告点击「保存分享图」时通过 `SaveButton` 安全控件触发一次性临时授权。
- 无账号体系、无广告、无内购、无第三方统计/推送 SDK；诊断由本地规则与算法引擎计算，不调用云端 AI。

## 推荐入口

- `docs/index.html`：GitHub Pages 首页，中文 / English 切换，隐私政策 / 用户协议切换。
- `privacy-policy.md`：中文隐私政策。
- `privacy-policy-en.md`：English privacy policy.
- `terms-of-service.md`：中文用户协议。
- `terms-of-service-en.md`：English terms of service.

## 兼容入口

以下大写文件名与推荐文件内容保持一致，保留以避免旧链接失效；修改协议正文时需同步更新两边：

- `PRIVACY_POLICY.md` -> `privacy-policy.md`
- `PRIVACY_POLICY_EN.md` -> `privacy-policy-en.md`
- `TERMS_OF_SERVICE.md` -> `terms-of-service.md`
- `TERMS_OF_SERVICE_EN.md` -> `terms-of-service-en.md`

## 部署说明

仓库已配置 `.github/workflows/pages.yml`，推送到 `main` 分支后自动部署 `docs/` 目录。

GitHub Pages 需在仓库 Settings -> Pages 中将 Source 设置为 `GitHub Actions`。

公开入口：

- 协议中心首页：https://tomkuku588-bot.github.io/mathtaxonomy/
- 隐私政策直达：https://tomkuku588-bot.github.io/mathtaxonomy/?doc=privacy
- 用户协议直达：https://tomkuku588-bot.github.io/mathtaxonomy/?doc=terms
- 英文版直达：在以上地址追加 `&lang=en`

AGC 提审时「隐私政策 URL」填写隐私政策直达地址。

## 关联远程

```
git remote add origin git@github.com:tomkuku588-bot/mathtaxonomy.git
git push -u origin main
```
