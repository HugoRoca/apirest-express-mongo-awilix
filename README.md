# API REST WITH DEPLOY IN HEROKU
[![Build Status](https://travis-ci.org/HugoRoca/apirest-express-mongo-awilix.svg?branch=master)](https://travis-ci.org/HugoRoca/apirest-express-mongo-awilix)

## Steps

- install travis (gem intall travis)
- install heroku and login (heroku login)
- view steps in heroku
- add `.travis.yml`
- exec this command:

```
travis encrypt $(heroku auth:token) --add deploy.api_key --org

or

travis encrypt <api-key> -r <github-user>/<repo-name> --add deploy.api_key

```

- complete travis file:

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
