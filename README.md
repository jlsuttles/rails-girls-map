Rails Girls Map
=============

## Deploy on Heroku

1. Move application to root directory.
```bash
$ mv represent-map/* .
$ rm -r represent-map
```

1. Create Heroku application.
```bash
$ heroku create rails-girls-map
```

1. Add MySQL database via ClearDB addon.
```bash
$ heroku addons:add cleardb:ignite
```

1. Configure database to use ClearDB.
```bash
$ cp include/db_example.php include/db.php
$ vi include/db.php # setup database variables
```
    - [Using ClearDB with PHP](https://devcenter.heroku.com/articles/cleardb#using-cleardb-with-php)

1. Set LD_LIBRARY_PATH
```bash
$ heroku config:set LD_LIBRARY_PATH="/app/php/ext"
```

1. Deploy
```bash
$ git push heroku
```

1. Create database tables.
