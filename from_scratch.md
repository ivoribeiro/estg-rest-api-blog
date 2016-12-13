##Laravel Scaffolding
1- Install laravel structure with composer

```composer create-project --prefer-dist laravel/laravel \<name>```

##Per Project Homestead

1- Install Homestead dependencies in your project

```composer require laravel/homestead --dev```

2- Configure Homestead in your project

```php vendor/bin/homestead make```

3- Add homestead.app to /etc/hosts


#Models && Migrations

##Make model and migration

``` php artisan make:model Category --migration ```

##Make just a migration

```php artisan make:migration create_post_table --create=post```

```php artisan make:migration create_comment_table --create=comment```

##Make just a model
```php artisan make:model Post```

```php artisan make:model Comment```


###Protect models 

To protect the application from mass assignment
```post
   /**
       * The attributes that are mass assignable.
       *
       * @var array
       */
      protected $fillable = ['<field_name>'];
```

##Migrate
```php artisan migrate```

##CRUD Controller

```php artisan make:controller CommentController --resource```

##Resource Route

Add the route to routes/api.php

```Route::resource('comments', 'CommentController',['except' => ['index']]);```


