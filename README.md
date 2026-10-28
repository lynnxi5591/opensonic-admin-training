# opensonic-admin-training

欧贲科技官网管理后台的培训 SKILL。装上以后，Claude 可以：

- 带新同事一课一课学后台；
- 回答「在哪改、怎么填、为什么保存不了、改了官网哪里会变」；
- 帮忙检查准备上架的内容。

## 目录

```
opensonic-admin-training/
  SKILL.md        培训 SKILL 本体（操作手册 + 课程 + 排错表），只改这一个文件
CHANGELOG.md      每次更新记一行，和后台版本对应
.github/workflows/release.yml   打 v 开头的标签时，自动打包 zip 发到 Releases
```

## 安装（给使用的同事）

1. 打开本仓库的 **Releases**，下载最新的 `opensonic-admin-training.zip`。
2. 在 Claude 的技能（Skills）设置里上传这个 zip。
3. 新开一个对话，说「我要学欧贲官网后台」或直接提问就能用。

同一个 claude.ai 组织里的同事，也可以由维护人直接把技能共享给他们，不用下载 zip。

## 维护（给维护人）

后台每次改版：

1. 在 Claude 的「OB 官网设计」项目里，把新的修改说明交给 Claude，让它更新 `opensonic-admin-training/SKILL.md`。
2. 在 `CHANGELOG.md` 加一行，把 SKILL.md 末尾「维护信息」里的版本号一起改掉。
3. 提交后打标签，比如 `v1.1.0`。GitHub 会自动打包 zip 发布到 Releases。
4. 通知同事重新下载安装，覆盖旧版本。

注意：这个仓库是**公开**的，只放培训内容，**不要放后台或前台的源码、`.env`、账号密码**。
