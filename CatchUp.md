# Learn Powerdey

## 2022-09-30
- Nestjs/angular monorepo using nx and yarn
- GitHub actions for CI/CD
	- run tests
	- lint code
	- report errors to slack
- Husky commit hooks

### Questions
Why does this cause the task graph to have dependencies like the project graph?
Text found [in](https://nx.dev/concepts/mental-model)
```json
{
  "test": {
    "executor": "@nrwl/jest:jest",
    "outputs": ["coverage/apps/app1"],
    "dependsOn": ["^test"],
    "options": {
      "jestConfig": "apps/app1/jest.config.js",
      "passWithNoTests": true
    }
  }
}
```
