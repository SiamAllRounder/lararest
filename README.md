## Before Activating sanctum on kernel api group you need to install then vendor publish sanctum service provider with artisan

# Basic Configuration Completed

```
C:\laragon\www\lararest(master -> origin)
λ php artisan migrate

   INFO  Running migrations.

  2023_07_04_164053_create_products_table ................................................................................................ 17ms DONE


C:\laragon\www\lararest(master -> origin)
λ
```
## migrated after edit migration

# Take A Controller Name Base Controller

```
C:\laragon\www\lararest(master -> origin)
λ php artisan make:controller BaseController

   INFO  Controller [C:\laragon\www\lararest\app/Http/Controllers/BaseController.php] created successfully.


C:\laragon\www\lararest(master -> origin)
λ
```

## Make Another New Controller RegisterController inside Api folder
```

C:\laragon\www\lararest(master -> origin)
λ php artisan make:controller Api\RegisterController

   INFO  Controller [C:\laragon\www\lararest\app/Http/Controllers/Api/RegisterController.php] created successfully.


C:\laragon\www\lararest(master -> origin)
λ

```
### take ProductController inside on api folder too
```
C:\laragon\www\lararest(master -> origin)
λ php artisan make:controller Api\ProductController

   INFO  Controller [C:\laragon\www\lararest\app/Http/Controllers/Api/ProductController.php] created successfully.


C:\laragon\www\lararest(master -> origin)
λ

```

# Laravel Rest API Bangla Tutorial Part I (Create Rest API from Scratch)

[Laravel Rest API Bangla Tutorial Part I (Create Rest API from Scratch) 819s](https://www.youtube.com/watch?v=bK-9vuZoLqc&t=819s)

# How to Build a REST API With Laravel: PHP Full Course

[How to Build a REST API With Laravel: PHP Full Course](https://www.youtube.com/watch?v=YGqCZjdgJJk)
##
## comment out this code
```
/* Route::middleware('auth:sanctum')->get('/user', function (Request $request) {
    return $request->user();
}); */
```
and add and refix this codes on api underneeth comment outed code

```
Route::post('register', [RegisterController::class, 'register']);
Route::post('login', [RegisterController::class, 'login']);

Route::group(['middleware' => 'auth:sanctum'], function () {
    Route::resource('products', ProductController::class);
});
```