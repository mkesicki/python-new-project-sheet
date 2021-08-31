Kudos to: https://mitelman.engineering/blog/python-best-practice/automating-python-best-practices-for-a-new-project/


```
poetry new my-project; cd my-project; ls
pyenv local 3.9.2
poetry env use python
poetry add --dev pytest-cov pre-commit flake8 mypy isort
poetry add --dev --allow-prereleases black
poetry shell
code .
```

```
echo '.coverage' > .gitignore
echo '.vscode/\n.idea/' >> .gitignore
curl -s https://raw.githubusercontent.com/github/gitignore/master/Python.gitignore >> .gitignore
git init -b main
git add .
git commit -m 'Initial commit'
pre-commit install
pre-commit autoupdate
pre-commit run --all-files
pre-commit run --all-files
```
