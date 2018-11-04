## Set up heroku (before setup heroku adding first your ssh key to your github account)
- Install heroku CLI [link](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
- open command line 
- login to your account `heroku login`
- adding keys to Heroku `heroku keys:add`
- validate the connection `ssh -v git@heroku.com`
- move to your directory project
- create heroku app `heroku create`
- setup nodejs version in project to deploy
open package.json
```
{
  ...
  "scripts": {
    ...
  },
  "engines": {
    "node": "6.2.2"
  },
  "author": "",
  ...
}
```
- add mongodb database `heroku addons:create mongolab:sandbox`
- add JWT_SECRET `heroku config:set JWT_SECRET=<input key secret you want>`
- config your database `heroku config`
- commit your code
- deploy your project `git push heroku master`

## Testing your endpoint
```
npm test
```

Download postman [environment](https://www.dropbox.com/s/4ihumh5yn7i1mgh/Todo%20App%20Heroku.postman_environment.json?dl=0) and [collection](https://www.dropbox.com/s/2wspzhjoj2403my/TodoApp.postman_collection.json?dl=0)



