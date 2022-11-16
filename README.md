# git-subtree-poc-project-a
POC subtre

## Howto

Extract folder into branch

```bash
$ git subtree split --prefix=packages/common --branch subtree/packages-common
```

Pull branch into bare repo

```bash
$ git pull ../git-subtree-poc-project-a subtree/packages-common
```

Replace folder with subtree

```bash
$ git subtree split --prefix=packages/common --branch subtree/packages-common
$ rm -rf packages/common
$ git add .
$ git commit -m "removed common package"
$ git subtree add --prefix=packages/common git@github.com:franklinkim/git-subtree-poc-common.git fork/project-a
```
