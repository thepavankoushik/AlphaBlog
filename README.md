# Project

[thepavankoushik-alphablog.herokuapp.com](thepavankoushik-alphablog.herokuapp.com)

**ALPHABLOG** is a platform where individuals or groups can share their thoughts, ideas, and experiences with the world through written content, known as blog posts. These posts can include text, images, and videos and are organized by date and often categorized by topic. This simple and clean AlphaBlog will have a minimalist design with easy navigation, allowing users to easily find and read blog posts. The website will also have features such as the ability to leave comments on posts and a search bar to help users find specific content. Overall, AlphaBlog is an accessible and user-friendly platform for individuals to share their thoughts and ideas with a wider audience.

## Install

### Clone the repository

```shell
git clone git@github.com:thepavankoushik/AlphaBlog.git
cd AlphaBlog
```

### Check your Ruby version

```shell
ruby -v
```

The ouput should start with something like `ruby 2.5.1`

If not, install the right ruby version using [rbenv](https://github.com/rbenv/rbenv) (it could take a while):

```shell
rbenv install 2.5.1
```

### Install dependencies

Using [Bundler](https://github.com/bundler/bundler) and [Yarn](https://github.com/yarnpkg/yarn):

```shell
bundle && yarn
```


### Initialize the database

```shell
rails db:create db:migrate db:seed
```

### Add heroku remotes

Using [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli):

```shell
heroku git:remote -a project
heroku git:remote --remote heroku-staging -a project-staging
```

## Serve

```shell
rails s
```

## Deploy

### With Heroku pipeline (recommended)

Push to Heroku staging remote:

```shell
git push heroku-staging
```

Go to the Heroku Dashboard and [promote the app to production](https://devcenter.heroku.com/articles/pipelines) or use Heroku CLI:

```shell
heroku pipelines:promote -a project-staging
```

### Directly to production (not recommended)

Push to Heroku production remote:

```shell
git push heroku
```
