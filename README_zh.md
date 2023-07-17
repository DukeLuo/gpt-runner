# GPT Runner（GPT运行器）

这个操作允许你在GitHub Actions中运行GPT Prompt。

## 如何开始

首先，你需要为这个操作设置一个名为`OPENAI_API_KEY`的action secret作为OpenAI API密钥。你可以在[这里](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository)找到更多关于如何设置的信息。

要在你的工作流中使用这个操作，你可以添加以下步骤：

```yaml
- name: 运行GPT Prompt
  uses: DukeLuo/gpt-runner@v1
  env:
    OPENAI_API_KEY: ${{ secrets.OPENAI_API_KEY }}
  with:
    cmd: promptr -p "整理src/index.js中的代码" # 指定你想要的GPT Prompt命令
```

你可以查看这个[完整的示例工作流](.github/workflows/gpt.yml)获取更多信息。

### 进一步阅读

- [Promptr](https://github.com/ferrislucas/promptr)