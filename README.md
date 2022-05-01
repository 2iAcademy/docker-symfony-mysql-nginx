# docker-symfony-postgres-nginx
A fully configured docker-compose environment for running a symfony app with postgres and nginx

### Setup

* Fork the repository
* Clone it
* In a terminal (use git bash for windows), cd into the directory cloned
* run the following command (**Replace your name and email** from the command)

```
docker run --rm -v $(pwd):$(pwd) -w $(pwd) -e "GIT_USERNAME=Your Name" -e "GIT_EMAIL=your@github.email" 2itech/php-symfony-cli symfony new app --webapp
```

--------------------------------------------------------------

##### After the project is created you can run

```
docker compose up -d
```

### Edit your hosts file

Your hosts file is located in :
* OSX / *unix => /etc/hosts
* Windows => C:/Windows/System32/Drivers/etc

Add the following:
```
127.0.0.1   m-2i-tech.academy
```

### Access it from your browser
Go to [http://m-2i-tech.academy](http://m-2i-tech.academy)

### Possible error
You may have an error where nginx is unable to write to cache and log directory.

If this happens, you can simply, from your Code Editor or your filesystem, delete the folders 'cache' and 'log' in your app/var folder.
