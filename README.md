# dsh-deepseek-hub

Sync DeepSeek web conversations into a local Markdown knowledge base through a controlled browser, and publish new DIY projects to GitHub.

DeepSeek Harness（DSH）插件。**本仓库是发布镜像**，源码与开发在 [DIY-code](https://github.com/YYY-DXS/DIY-code) 的 plugins/deepseek-hub/；两份内容由 	ools/publish-plugin.ps1 同步，不要只改这里。

## 安装

```bash
dsh plugin add github:YYY-DXS/dsh-deepseek-hub
```

安装后在 **设置 → 插件** 里确认该行已启用；首次使用前按下面「配置」填好路径。

## 配置

```yaml
- insert:
    - id: deepseek-hub
      name: 'dsh-deepseek-hub'
      config:
        # 改成你自己的路径；也可以不填，用环境变量 DEEPSEEK_HUB_KNOWLEDGE 等覆盖
        knowledgeDir: 'C:\path\to\knowledge\deepseek-web'
        profileDir: 'C:\path\to\deepseek-hub-profile'
        edgePath: 'C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe'
        repoDir: 'C:\path\to\DIY-code'
        pythonPath: ''
        port: 9390
        autoSyncMinutes: 60
        dailyPublishAt: '20:00'
```

## 兼容性

- DSH：`>=0.1.0-rc.6 <0.3.0-0`
- Node：`>=18`
- 平台：Windows

## 许可

MIT，见 [LICENSE](LICENSE)。