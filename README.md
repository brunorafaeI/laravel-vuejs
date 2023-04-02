# Introduction

A simple project built with Laravel 10.x using sail to setup a boilerpate composed with : <br />
- pgsql
- redis
- meilisearch
- mailpit
- selenium

## Get Started

Install a new project Laravel :

```sh
curl -s https://laravel.build/backend?with=pgsql,redis,meilisearch,mailpit,selenium | bash
```

You can source the custom alias, instead of repeatedly typing `vendor/bin/sail` to execute Sail and Docker commands, you may wish to configure a shell alias that allows you to execute Sail's commands more easily

Make it permanently accessible inside the `.bashrc` file
```sh
cat docker/alias.sh >> ~/.bashrc 
source ~/.bashrc
```
*Note: You can create more alias before append it  into your shell*


let's try it, go to the project root directory and execute the following command :

```sh
cd backend && sail up -d # flag -d to run the command on mode dettached.
```

## Working with Vuejs or Reactjs (Starter kits)

### Installing [Breeze and React/Vue](`https://laravel.com/docs/10.x/starter-kits#breeze-and-inertia`)

```sh
composer require laravel/breeze --dev
``` 

Now you can implement React or Vue scaffolding via an [Inertia](`https://inertiajs.com/`) frontend implementation

```sh
php artisan breeze:install vue
 
# Or...
 
php artisan breeze:install react
 
php artisan migrate
npm install
npm run dev
``` 
Next, you may navigate to your application's **/login** or **/register** URLs in your web browser. All of Breeze's routes are defined within the **routes/auth.php** file.

## Initial configuration

For more information to configuration your application take a look at the documentation [Laravel -> Initial Configuration](`https://laravel.com/docs/10.x#initial-configuration`)

Make sure you have put correctly settings in your `.env` :
In the case you are not using localhost, you will need to set your environment, for instance:

```
APP_URL=http://my-own-domain.com
ASSET_URL=http://my-own-domain.com
```