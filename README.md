# ming-career-mini-web

《大明仕途录》的静态发布仓库。

- 源码仓库：`ReZeroWorks/ming-career-mini`（Private）
- 本仓库：仅承载构建后的 `dist` 静态产物和 Pages 发布 workflow
- 目标访问地址：`https://rezeroworks.github.io/ming-career-mini-web/`

## 可见性要求

要让老师无需 GitHub 登录直接访问，本仓库必须设为 **Public**。源码仓库继续保持 Private。

## 自动发布设计

Private 源码仓库 CI 负责测试和构建。跨仓库自动同步不能直接依赖默认 `GITHUB_TOKEN`，因为它的权限局限于当前仓库。后续使用 GitHub App / fine-grained PAT（仅授予本发布仓库 Contents: write）完成自动同步；在配置凭据前，不添加虚假的跨仓库 push workflow。

