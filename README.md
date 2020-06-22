# API REST WITH DEPLOY IN HEROKU
[![Build Status](https://travis-ci.org/HugoRoca/apirest-express-mongo-awilix.svg?branch=master)](https://travis-ci.org/HugoRoca/apirest-express-mongo-awilix)

## Steps

1- install travis (gem intall travis)
2- install heroku and login (heroku login)
3- view steps in heroku
4- add `.travis.yml`
5- exec this command:

```
travis encrypt $(heroku auth:token) --add deploy.api_key --org

or

travis encrypt <api-key> -r <github-user>/<repo-name> --add deploy.api_key

```

6- complete travis file:

```yaml
language: node_js
node_js:
  - stable
deploy:
  provider: heroku
  app: myfirstapiheroku-nodejs
  api_key:
    secure: xxx
```
