# GPT Runner

This action allows you to run GPT prompt for your codebase from GitHub Actions.

## How to start

Firstly, you need to set OpenAI API Key with a action secret named `OPENAI_API_KEY` for this action. You can find more information about how to do it [here](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository).

To use this action in your workflow, you can add the following step:

```yaml
- name: Run GPT Prompt
  uses: DukeLuo/gpt-runner@v1.0.0
  env:
    OPENAI_API_KEY: ${{ secrets.OPENAI_API_KEY }}
  with:
    cmd: promptr -p "Cleanup the code in src/index.js" # Specify your desired GPT Prompt command
```

You can check out this [full example workflow](.github/workflows/gpt.yml) for more information.

### Further Reading

- [Promptr](https://github.com/ferrislucas/promptr)
