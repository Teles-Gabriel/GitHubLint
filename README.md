# GitHubLint
Repositório para testar o uso do Commitlint, Husky e Commitizen.
Essas ferramentas servem para padronizar as mensagens de commits visando melhorar e facilitar o entendimento do histórico de commits.

## Para devs

  Para instalar as ferramentas, eu utilizei majoritariamente o tutorial disponível nesse link (<a href="https://medium.com/@vinicius.oliver/guia-completo-para-padroniza%C3%A7%C3%A3o-de-commits-commitlint-husky-e-commitizen-c9b76dc6cc2b">TUTORIAL</a>)

  <a href="https://github.com/commitizen/cz-cli">Aqui você pode encontrar a documentação de instalação do commitzen.</a>

  <a href="https://github.com/conventional-changelog/commitlint">O Commitlint está disponivel aqui.</a>

  <a href="https://typicode.github.io/husky/">O Husky está disponivel aqui.</a>

## Algumas alterações para ficar atento no `package.json`: 

```
"scripts": {
    "commit": "git-cz",
    "prepare": "husky install",
    "test": "echo \"Error: no test specified\" && exit 1"
  }
```

  ```
  "husky": {
    "hooks": {
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
    }
  }
  ```

```
  "devDependencies": {
      "@commitlint/cli": "^19.3.0",
      "@commitlint/config-conventional": "^19.2.2",
      "commitizen": "^4.3.0",
      "cz-conventional-changelog": "^3.3.0",
      "husky": "^9.0.11"
    }
```

```
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    }
  }
```
