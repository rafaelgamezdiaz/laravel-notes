### Install the project with Sail

```
curl -s "https://laravel.build/example-app?with=mysql" | bash
```

### Change DB credentials

When installing a new Laravel project with Sail it is possible to change
credentials to the DB inside the container.

edit the .env, ex.:

```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=bookstore_db
DB_USERNAME=admin_bs
DB_PASSWORD=Jmb9w7L.h6aj
```

then

```
sail down -v
sail build --no-cache
sail up -d
```

Now you can access to the database

```
sail mysql -u admin_bs -p Jmb9w7L.h6aj
```

### Install passport

```
sail composer require laravel/passport

sail php artisan passport:install
```

example console output:
```
  Encryption keys generated successfully.
  Personal access client created successfully.
  Client ID: 1
  Client secret: Hp5SSOR9m9XiQDIci0UoIlebRhl82RWdWft9DIlO
  Password grant client created successfully.
  Client ID: 2
  Client secret: n2xHK5wS3EuEO85zGqorINc1bYHdVyN8i7Onvbbg
```