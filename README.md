`poetry install` will fail if some dependencies has the same Git repository?
===================================================================================

```toml
[tool.poetry.dependencies]
quri-parts-qulacs = { git = "https://github.com/QunaSys/quri-parts.git", rev = "3b05ea12dede01b9bea70b0fbecb246ca3167639", subdirectory = "packages/qulacs" }
quri-parts-qiskit = { git = "https://github.com/QunaSys/quri-parts.git", rev = "3b05ea12dede01b9bea70b0fbecb246ca3167639", subdirectory = "packages/qiskit" }
quri-parts-stim = { git = "https://github.com/QunaSys/quri-parts.git", rev = "3b05ea12dede01b9bea70b0fbecb246ca3167639", subdirectory = "packages/stim" }
```

But it will success when `rm poetry.lock` before `poetry install`🤔🤔🤔

## Example Result

- https://github.com/y-yu/poetry-conflict-test/actions/runs/5236988803
